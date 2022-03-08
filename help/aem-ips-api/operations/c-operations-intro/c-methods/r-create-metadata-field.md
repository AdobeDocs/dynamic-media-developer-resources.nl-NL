---
description: Hiermee kunnen beheerders nieuwe metagegevensvelden maken voor coördinatie met contentbeheersystemen of voor sjabloonbewerkingen. Voorbeelden van gemaakte metagegevensvelden zijn trefwoorden, informatie over de auteur van de afbeelding of informatie over de copyrighthouder.
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# createMetadataField{#createmetadatafield}

Hiermee kunnen beheerders nieuwe metagegevensvelden maken voor coördinatie met contentbeheersystemen of voor sjabloonbewerkingen. Voorbeelden van gemaakte metagegevensvelden zijn trefwoorden, informatie over de auteur van de afbeelding of informatie over de copyrighthouder.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parameters {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Input (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Naam van het bedrijf waartoe het metagegevensveld behoort. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Elementtype. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Naam van het metagegevensveld dat u maakt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Type metagegevensveld. <p>De constante typen metagegevensvelden definieert de beschikbare typen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>De standaardwaarde van het metagegevensveld dat moet worden gemaakt (bijvoorbeeld <span class="codeph"> Scène 7</span>). </p> <p>Standaardwaarden worden niet ondersteund voor typen tagvelden en moeten worden weggelaten. Als een niet-lege standaardinstelling is opgegeven voor een type tagveld, wordt een fout geretourneerd. </p> </td> 
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
   <td colname="col4"> Hiermee kunt u een set gedeelde opsommingswaarden maken waarnaar geselecteerde tags kunnen wijzen. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createMetadataFieldReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | De greep naar het nieuwe metagegevensveld. |

## Voorbeelden {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

In dit codevoorbeeld wordt een metagegevensveld voor tekenreekstypen gemaakt met de naam `createMetadataField`. De reactie keert de handvat op het nieuwe meta-gegevensgebied terug.

**Verzoek**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Antwoord**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```
