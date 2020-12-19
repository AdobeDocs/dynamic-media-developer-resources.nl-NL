---
description: Maak of bewerk een metagegevensveld. Laat de optionele veldgreep weg om een nieuw metagegevensveld te maken.
seo-description: Maak of bewerk een metagegevensveld. Laat de optionele veldgreep weg om een nieuw metagegevensveld te maken.
seo-title: saveMetadataField
solution: Experience Manager
title: saveMetadataField
topic: Scene7 Image Production System API
uuid: ccd84366-732a-4caf-914d-3bc5fe499e7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# saveMetadataField{#savemetadatafield}

Maak of bewerk een metagegevensveld. Laat de optionele veldgreep weg om een nieuw metagegevensveld te maken.

>[!NOTE]
>
>Deze methode is afgekeurd.

## Toegestane gebruikerstypen {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-ec6827d485a143f4a059a92b18e40f4e}

**Input (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameternaam </th> 
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
   <td colname="col4"> De handgreep aan het bedrijf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Veldgreep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Keuze van elementtypen waaruit metagegevens moeten worden opgeslagen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Veldnaam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Keuze van veldtypen voor metagegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Standaardwaarde van de velden voor alle elementen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> De huid of stelt IPS systeem-specifieke meta-gegevens bloot. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforce</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Een Booleaanse markering die aangeeft of het metagegevensveld wordt afgedwongen (gevalideerd) wanneer de waarde wordt ingesteld. </p> <p>Indien ingesteld op true, wordt een fout gegenereerd als een ongeldige waarde is ingesteld in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (saveMetadataFieldReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Ja | Handgreep van het nieuwe metagegevensveld. |

## Voorbeelden {#section-4441c26d1f41466ba972b43dd5189e89}

In dit codevoorbeeld wordt een nieuw metagegevensveld gemaakt dat wordt beperkt door de tekenreeksconstanten voor elementtype en metagegevenstypen. Als het element `fieldHandle` een geldige waarde voor de veldgreep heeft, worden de metagegevenswaarden gewijzigd en wordt dezelfde veldgreep opgehaald die u in de aanvraag hebt opgegeven.

**Verzoek**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**Antwoord**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```

