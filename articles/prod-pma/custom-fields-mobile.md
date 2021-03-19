---
title: iOS ve Android cihazlarda Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulama
description: Bu konuda, özel alanları uygulamak üzere uzantıları kullanmak için yaygın kalıplar sağlanır.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271017"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>iOS ve Android cihazlarda Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulama

[!include [banner](../includes/banner.md)]

Bu konuda, özel alanları uygulamak üzere uzantıları kullanmak için yaygın kalıplar sağlanır. Aşağıdaki konular ele alınmıştır:

- Özel alan çerçevesinin desteklediği çeşitli veri türleri
- Zaman çizelgesi girişlerinde salt okunur veya düzenlenebilir alanları gösterme ve kullanıcı tarafından sağlanan değerleri veritabanına yeniden kaydetme
- Zaman çizelgesi üstbilgisindeki salt okunur alanlar nasıl gösterilir
- Diğer özel iş mantığı, alanlara varsayılan değerler girmek için nasıl tümleştirilir ve ek doğrulama yapılır

## <a name="audience"></a>Hedef Kitle

Bu konu, Apple iOS ve Google Android cihazlarda kullanılabilen Microsoft Dynamics 365 Project Timesheet mobil uygulamasıyla özel alanlarını tümleştiren geliştiriciler içindir. Okuyucuların X++ geliştirme ve proje zaman çizelgesi işlevleriyle ilgili bilgi sahibi olduğu varsayılmıştır.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Veri sözleşmesi – TSTimesheetCustomField X + + sınıfı

**TSTimesheetCustomField** sınıfı, zaman çizelgesi işlevselliği için özel bir alanla ilgili bilgileri temsil eden X++ veri sözleşmesi sınıfıdır. Özel alan nesnelerinin listeleri, mobil uygulamadaki özel alanları göstermek için hem TSTimesheetDetails veri sözleşmesine hem de TSTimesheetEntry veri sözleşmesine aktarılır.

- **TSTimesheetDetails**: zaman çizelgesi başlığı sözleşmesi.
- **TSTimesheetEntry**: zaman çizelgesi hareket sözleşmesi. Aynı proje bilgilerine ve **timesheetLineRecId** değerine sahip olan bu nesnelerin grupları bir satır oluşturur.

### <a name="fieldbasetype-types"></a>fieldBaseType (Türler)

**TsTimesheetCustom** nesnesindeki **FieldBaseType** özelliği, uygulamada görünen alanın türünü belirler. Aşağıdaki **Türler** değerleri desteklenir.

| Türler değeri | Tür              | Notlar |
|-------------|-------------------|-------|
| 0           | Dize (ve Enum) | Alan, bir metin alanı olarak görüntülenir. |
| 1           | Integer           | Değer, ondalık basamak olmayan bir sayı olarak gösterilir. |
| 2           | Gerçek sayı              | Değer, ondalık basamağı olan bir sayı olarak gösterilir.<p>Gerçek değeri uygulamada bir para birimi olarak göstermek için, **fieldExtenededType** özelliğini kullanın. Gösterilen ondalık basamak sayısını ayarlamak için **numberOfDecimals** özelliğini kullanabilirsiniz.</p> |
| 3           | Tarih              | Tarih biçimleri, **Kullanıcı seçenekleri** bölümünde **Dil ve ülke/bölge tercihi** altında belirtilen kullanıcının **Tarih, zaman ve sayı biçimi** ayarından belirlenir. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- **TSTimesheetCustomField** nesnesinde **stringOptions** özelliği verilmemişse, kullanıcıya serbest metin alanı sağlanır.

    **stringLength** özelliği, kullanıcıların girebileceği en fazla dize uzunluğunu ayarlamak için kullanılabilir.

- **TSTimesheetCustomField** nesnesinde **stringOptions** özelliği verilmişse, kullanıcıların seçenek düğmelerini (radyo düğmeleri) kullanarak seçim yapmasına yönelik değerler yalnızca bu liste öğelerinden oluşur.

    Bu durumda, dize alanı kullanıcı giriş yapmasına yönelik bir Enum değeri olarak işlev görebilir. Değeri veritabanına enum olarak kaydetmek için, komut zincirini kullanarak veritabanına kaydetmeden önce dize değerini el ile enum değerine tekrar eşleştirin. (Örnek için bu konu içinde ilerleyen bölümlerde yer alan "Uygulamadan zaman çizelgesi girişini yeniden veritabanına kaydetmek için TSTimesheetEntryService sınıfında komut zincirini kullanma" bölümüne bakın.)

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Bu özelliği, gerçek değerleri para birimi olarak biçimlendirmek için kullanabilirsiniz. Bu yaklaşım yalnızca **fieldBaseType** değeri **Gerçek** olduğunda uygulanabilir.

- **TSCustomFieldExtendedType:None**: Hiçbir biçimlendirme uygulanmaz.
- **TSCustomFieldExtendedType::Para birimi**: Değeri para birimi olarak biçimlendirir.

    Para birimi olarak biçimlendirme etkin olduğunda, **stringValue** alanı, uygulamada gösterilmesi gereken para birimi kodunu aktarmak için kullanılabilir. Salt okunur bir değerdir.

    **realValue** alanı, veritabanına kaydedilmesi gereken para tutarını içerir.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Özel alanın uygulamada nerede görüntüleneceğini belirtmek için bu özelliği kullanabilirsiniz.

- **TsccustomFieldSection::Başlık**: Alan, uygulamada **Daha fazla ayrıntı görüntüle** bölümünde gösterilir. Bu alanlar her zaman salt okunurdur.
- **TSCustomFieldSection::Satır**: Alan, zaman çizelgesi girişlerindeki tüm hazır satır alanlarından sonra görüntülenir. Bu alanlar düzenlenebilir ya da salt okunur olabilir.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Bu özellik, uygulamanın sağladığı değerlerin veritabanına tekrar ne zaman kaydedileceğini tanımlar.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Bu özellik, uygulamanın sağladığı değerlerin veritabanına tekrar ne zaman kaydedileceğini tanımlar.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Zaman çizelgesi girişi bölümündeki alanının kullanıcılar tarafından düzenlenebilir olması gerektiğini belirtmek için bu özelliği **Evet** olarak ayarlayın. Alanı salt okunur yapmak için, özelliğini **Hayır** olarak ayarlayın.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Zaman çizelgesi girişi bölümündeki alanının zorunlu olması gerektiğini belirtmek için bu özelliği **Evet** olarak ayarlayın.

### <a name="label-str"></a>label (str)

Bu özellik, uygulamadaki alanların yanında gösterilen etiketi belirtir.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Dize Listesi)

Bu özellik yalnızca **fieldBaseType** alanı **String** olarak ayarlandığında uygulanabilir. **stringOptions** ayarlanmışsa, seçenek düğmeleri (radyo düğmeleri) aracılığıyla seçim için kullanılacak dize değerler listedeki dizeler ile belirtilir. Herhangi bir dize verilmezse, dize alanında serbest metin girdisine izin verilir. (Örnek için bu konu içinde ilerleyen bölümlerde yer alan "Uygulamadan zaman çizelgesi girişini yeniden veritabanına kaydetmek için TSTimesheetEntryService sınıfında komut zincirini kullanma" bölümüne bakın.)

### <a name="stringlength-int"></a>stringLength (int)

Bu özellik bir dize alanındaki en fazla uzunluğu belirtir. Yalnızca **fieldBaseType** alanı **String** olarak ayarlandığında uygulanabilir.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Bu özellik, gerçek bir alan için gösterilen ondalık basamak sayısını belirtir. Yalnızca **fieldBaseType** alanı **Gerçek** olarak ayarlandığında uygulanabilir.

### <a name="ordersequence-int"></a>orderSequence (int)

Bu özellik birden çok özel alan belirtildiğinde, özel alanların uygulamada gösterilme sırasını denetler. Daha küçük sayılar içeren alanlar önce gösterilir.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Bu özellik, **Boolean** türündeki alanlar için, alanın Boolean değerini sunucu ile uygulama arasında iletir.

### <a name="guidvalue-guid"></a>guidValue (guid)

Bu özellik, **GUID** türündeki alanlar için, alanın genel benzersiz tanımlayıcı (GUID) değerini sunucu ile uygulama arasında iletir.

### <a name="int64value-int64"></a>int64Value (int64)

Bu özellik, **Int64** türündeki alanlar için, alanın int64 değerini sunucu ile uygulama arasında iletir.

### <a name="intvalue-int"></a>intValue (int)

Bu özellik, **Int** türündeki alanlar için, alanın int değerini sunucu ile uygulama arasında iletir.

### <a name="realvalue-real"></a>realValue (real)

Bu özellik, **Gerçek** türündeki alanlar için, alanın gerçek sayı değerini sunucu ile uygulama arasında iletir.

### <a name="stringvalue-str"></a>stringValue (str)

Bu özellik, **Dize** türündeki alanlar için, alanın dize değerini sunucu ile uygulama arasında iletir. Ayrıca, para birimi olarak biçimlendirilmiş **Gerçek** alanları için de kullanılır. Bu alanlar için, söz konusu özellik para birimi kodunu uygulamaya iletmek amacıyla kullanılır.

### <a name="datevalue-date"></a>dateValue (date)

Bu özellik, **Tarih** türündeki alanlar için, alanın tarih değerini sunucu ile uygulama arasında iletir.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Zaman çizelgesi girişi bölümünde özel alan gösterme ve kaydetme

Aşağıda, bir zaman çizelgesi girişi oluşturma sırasında mobil uygulamadan alınan bir ekran görüntüsü yer alınır. "Zaman girişi" bölümündeki kullanıma hazır alanlar ile daha önceden ayarlanmış "Second option" enum değerine sahip "Test string" adlı özel bir alan gösterilir.

![Uygulamadaki Test string özel alanı](media/timesheet-entry.jpg)



Aşağıdaki ekran görüntüsü, "Test string" özel alanı için verilen enum seçeneklerinden birini belirleyen kullanıcının mobil uygulamasından alınmıştır.  Bu iki seçenek, radyo düğmeleri olarak gösterilen "First option" ve "Second option" seçenekleridir. İkinci seçenek seçilidir.

![Test string özel alanı için seçenek düğmeleri (radyo düğmeleri)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Özel bir alanı olması için TSTimeheetLine tablosunu genişletme

Tipik senaryolarda, zaman çizelgesi girişi bölümündeki özel alana ait veriler TSTimesheetLine tablosuna kaydedilebilir. Ancak, veriler sağlanan bir TSTimesheetTrans kaydına bağlı olarak getirildiğinde veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.

Özel alanların veritabanı kayıtlarının yedeğinin alınmasının zorunlu olmadığını unutmayın. Bunlar X++ mantığına bağlı olarak dinamik şekilde oluşturulabilir. Bu yaklaşım, salt okunur senaryolarda yararlı olabilir. (Dinamik olarak üretilen özel alan değerleri ile ilgili örnek için "Zaman çizelgesi ayrıntılarını doldurmak için TSTimesheetDetails sınıfı, buildCustomFieldListForHeader yönteminde komut zincirini kullanma" bölümüne bakın.)

Aşağıdaki ekran görüntüsü Uygulama Nesne Ağacı'nın Visual Studio öğesine aittir. Özel alan olarak eklenmiş TestLineString alanı bulunan TSTimesheetLine tablosunun bir uzantısını gösterilmektedir.

![Satır dizesi](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Zaman çizelgesi girişi bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zinciri kullanma

Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler. Örneğin, alan türünü, etiketi, alanın zorunlu olup olmadığını ve alanın hangi bölümünde görüntüleneceğini denetler.

Aşağıdaki örnekte zaman girişlerinde bir dize alanı gösterilmektedir. Bu alanda, seçenek düğmeleri (radyo düğmeleri) aracılığıyla kullanılabilen **First option** ve **Second option** olan iki seçenek bulunur. Uygulamadaki alan, TSTimesheetLine tablosuna eklenen **TestLineString** alanıyla ilişkilidir.

Özel alan özelliklerinin başlatılmasını kolaylaştıracak **TSTimesheetCustomField::newFromMetatdata()** yönteminin kullanımına dikkat edin: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ve **numberOfDecimals**. Ayrıca, bu parametreleri dilerseniz el ile de ayarlayabilirsiniz.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Zaman çizelgesi girişine değer girmek için TSTimesheetEntry sınıfının buildCustomFieldListForEntry yönteminde komut zinciri kullanma

**buildCustomFieldListForEntry** yöntemi, mobil uygulamadaki kaydedilmiş zaman çizelgesi satırlarına değer girmek için kullanılır. Parametre olarak bir TSTimesheetTrans kaydı alır. Bu kayıttaki alanlar, uygulamadaki özel alan değerini doldurmak için kullanılabilir.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Uygulamadan zaman çizelgesi girişini yeniden veritabanına kaydetmek için TSTimesheetEntryService sınıfında komut zincirini kullanma

Tipik kullanımda özel alanı veritabanına tekrar kaydetmek için, birden çok yöntem genişletmeniz gerekir:

- **timesheetLineNeedsUpdating** yöntemi, satır kaydının uygulamadaki kullanıcı tarafından değiştirilip değiştirilmediğini ve veritabanına kaydedilmesi gerekip gerekmediğini belirlemek için kullanılır. Performans sorun değilse, bu yöntem basitleştirilebilir. Böylece her zaman **doğru** sonucu döner.
- **populateTimesheetLineFromEntryDuringCreate** ve **populateTimesheetLineFromEntryDuringUpdate** yöntemleri, sağlanan TSTimesheetEntry veri sözleşmesi kaydından TSTimesheetLine veritabanı kaydına değer girilmesi için genişletilebilir. Aşağıdaki örnekte, veritabanı alanıyla giriş alanı arasındaki eşlemenin X++ kodu aracılığıyla el ile nasıl yapıldığı konusunda dikkat edin.
- **populateTimesheetWeekFromEntry** yöntemi, **TSTimesheetEntry** nesnesiyle eşlenen özel alanın TSTimesheetLineweek veritabanı tablosuna yeniden yazması için de genişletilebilir.

> [!NOTE]
> Aşağıdaki örnekte, kullanıcının seçtiği **firstOption** veya **secondOption** değeri veritabanına ham dize değeri olarak kaydedilir. Veritabanı alanı **Enum** türünde bir alan ise, bu değerler el ile bir enum değerine eşleştirilebilir ve sonra veritabanı tablosundaki bir enum alanına kaydedilebilir.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Zaman çizelgesi başlık bölümünde özel alan gösterme

Aşağıda; mobil uygulamadan alınan, zaman çizelgesini görüntüleyen bir kullanıcıya ait bir ekran görüntüsü yer alınır. "Daha fazla ayrıntı görüntüle" seçeneğini göstermek için, sağ üst köşedeki "Daha fazla bilgi" düğmesi seçilmiştir.  

![Daha fazla ayrıntı görüntüle komutu](media/show-more.png)

Aşağıda; zaman çizelgesindeki "Daha fazla" bölümünün gösterildiği mobil uygulamadan alınan bir ekran görüntüsü yer alınır. "Utilization rate of this timesheet (computed custom field)" adlı özel alan, zaman çizelgesi başlığı bölümüne eklendi. Özel alanda salt okunur olan "0,667" değeri ayarlanır.

![Daha fazla bölümü](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Özel bir alanı olması için TSTimesheetTable tablosunu genişletme

Tipik senaryolarda, başlık bölümündeki özel alana ait veriler TSTimesheetHeader tablosundan çekilebilir. Ancak, veriler sağlanan bir TSTimesheetTable kaydına bağlı olarak getirildiğinde veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.

Özel alanların veritabanı kayıtlarının yedeğinin alınmasının zorunlu olmadığını unutmayın. Bunlar X++ mantığına bağlı olarak dinamik şekilde oluşturulabilir. Aşağıdaki örnek bu yaklaşımı gösterir.

Başlık bölümündeki alanlar uygulamada her zaman salt okunurdur.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Başlık bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zincirini kullanma

Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler. Örneğin, alan türünü, etiketi, alanın zorunlu olup olmadığını ve alanın hangi bölümünde görüntüleneceğini denetler.

Aşağıdaki örnekte, uygulamadaki başlık bölümünde hesaplanan bir değer gösterilir.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Zaman çizelgesi ayrıntılarını doldurmak için TSTimesheetEntry sınıfının buildCustomFieldListForEntry yönteminde komut zincirini kullanma

**buildCustomFieldListForHeader** yöntemi, mobil uygulamadaki zaman çizelgesi başlık ayrıntılarını doldurmak için kullanılır. Parametre olarak bir TSTimesheetTable kaydı alır. Bu kayıttaki alanlar, uygulamadaki özel alan değerini doldurmak için kullanılabilir. Aşağıdaki örnekte, veritabanından değer okunmaz. Bunun yerine, uygulamada gösterilen hesaplanan bir değer oluşturmak için X++ mantığını kullanır.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Diğer yapılandırılabilirlik/genişletilebilirlik fırsatları

### <a name="adding-additional-validation-for-the-app"></a>Uygulama için ek doğrulama ekleme

Veritabanı düzeyindeki zaman çizelgesi işlevselliği için var olan mantık, beklendiği gibi çalışmaya devam eder. Kaydetme veya gönderme işlemlerinin tamamlanmasını kesmek ve belirli bir hata iletisini göstermek için komut zinciri uzantısı aracılığıyla koda **hata oluştu ("kullanıcıya ileti")** iletisi ekleyebilirsiniz. Yararlı genişletilebilir yöntemlerle ilgili üç örnek:

- Bir zaman çizelgesi satırı için kaydetme işlemi sırasında TSTimesheetLine tablosunda **validatewrite** **false** değerini döndürürse, mobil uygulamada bir hata iletisi görüntülenir.
- Bir zaman çizelgesi satırı için gönderme işlemi sırasında TSTimesheetTable tablosunda **validateSubmit** **false** değerini döndürürse, kullanıcıya hata iletisi gösterilir.
- **insert** yöntemi sırasında, TSTimesheetLine tablosundaki alanları (örneğin, **Satır Özelliği**) dolduran mantık çalışmaya devam eder.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Kullanıma hazır alanları yapılandırma aracılığıyla salt okunur olarak gizleme ve işaretleme

Proje parametrelerinden, kullanıma hazır alanları mobil uygulamada salt okunur veya gizli yapabilirsiniz. **Proje yönetimi ve muhasebe parametreleri** sayfasının **Zaman çizelgesi** sekmesindeki **Mobil zaman çizelgeleri** bölümünden seçenekleri ayarlayın.

![Proje parametreleri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Uzantılar aracılığıyla seçim için verilen etkinlikleri değiştirme

Bir projede seçim için verilen etkinlikler, **TsTimesheetProjectService** sınıfındaki **getActivitiesForProject()** ve **getActivityQuery()** yöntemleriyle doldurulur. Belirli bir projede seçim için verilen etkinlikler için bu davranışı iş senaryosuyla eşleşecek şekilde değiştirmek üzere komut zincirini kullanabilirsiniz.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Zaman çizelgesi girişlerine varsayılan proje kategorisi girme

Zaman çizelgesi girişlerinde varsayılan proje kategorisi girişi üç düzeyde oluşur. İstediğiniz davranışı elde etmek için bu düzeylerin herhangi birinin veya tümünün davranışını uzatmak amacıyla komut zincirini kullanabilirsiniz. Aşağıdaki hiyerarşi kullanılır:

1. Uygulama, proje kaynağından varsayılan kategoriyi yerleştirmeye çalışır. Bu varsayılan kategori, **TSTimesheetSettingsService** sınıfındaki **getCurrentUserResource** ve **getDelegatedResourcesForCurrentUser** yöntemlerinde ayarlanır.
2. Proje kaynak düzeyinde varsayılan kategori sağlanmamışsa, uygulama proje etkinliğinden almaya çalışır. Bu varsayılan kategori, **TSTimesheetProjectService** sınıfındaki **getActivitiesForProject** yönteminde ayarlanır.
3. Proje etkinlik düzeyinde varsayılan kategori sağlanmamışsa, varsayılan kategori proje parametrelerinden alınır. Bu varsayılan kategori, **TSTimesheetProjectService** sınıfındaki **getProjectDetailsbyRule** yönteminde ayarlanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]