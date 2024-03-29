---
description: Hiermee werkt u de tagwoordenboekwaarden voor een tagveld bij.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# updateTagFieldValues{#updatetagfieldvalues}

Hiermee werkt u de tagwoordenboekwaarden voor een tagveld bij.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-0a3a4bab026746238c9d4009caf42e94}

**Input (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Vereist </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Bedrijfshandgreep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handgreep van tagveld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Array met waarden voor tagvelden die u wilt bijwerken. <p>Opmerking: Hiermee werkt u alleen tekenreekswaarden bij. Dit heeft geen invloed op de activaverenigingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateTagFieldValuesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Het aantal correct bijgewerkte tagvelden. |
| warningCount | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking probeerde tagvelden bij te werken. |
| errorCount | `xsd:int` | Ja | Het aantal fouten dat is gegenereerd toen de bewerking probeerde tagvelden bij te werken. |
| warningDetailArray | `types:TagValueUpdateFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde tagvelden bij te werken. |
| errorDetailArray | `types:TagValueUpdateFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde tagvelden bij te werken. |

## Voorbeelden {#section-bb4dcf97044c4675974c9b8d27674001}

**Verzoek**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Antwoord**

```java {.line-numbers}
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```
