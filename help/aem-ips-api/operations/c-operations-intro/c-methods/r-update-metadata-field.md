---
description: Metagegevens van velden bijwerken.
seo-description: Metagegevens van velden bijwerken.
seo-title: updateMetadataField
solution: Experience Manager
title: updateMetadataField
topic: Scene7 Image Production System API
uuid: 8712b09b-b02a-4fb3-a0ed-084dc48a717a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# updateMetadataField{#updatemetadatafield}

Metagegevens van velden bijwerken.

Syntaxis

## Toegestane gebruikerstypen {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-69681ed1ddff437ca1c73f46fe835c96}

**Input (updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
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
   <td colname="col4"> Bedrijfshandgreep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handgreep metagegevensveld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Naam metagegevensveld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Waarde van metagegevensveld. </td> 
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
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Hiermee kunt u een set gedeelde opsommingswaarden maken waarnaar geselecteerde tags kunnen verwijzen. </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateMetadataFieldReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Ja | Handgreep metagegevensveld. |

## Voorbeelden {#section-bb7d93ab6d914ddfa294e08983e589ee}

In deze codevoorbeeldupdates worden een nieuwe naam en standaardwaarde toegewezen aan een metagegevensveld. De reactie retourneert een greep naar het bijgewerkte veld.

**Verzoek**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**Antwoord**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

