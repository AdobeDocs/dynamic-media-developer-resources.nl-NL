---
description: Zoek naar activa die op uw gespecificeerde criteria worden gebaseerd.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# searchAssets{#searchassets}

Zoek naar activa die op uw gespecificeerde criteria worden gebaseerd.

Syntaxis

## searchAssets: Info {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` is de primaire methode om IPS activa terug te winnen. Deze methode wordt gebruikt voor verschillende doeleinden, zoals het bladeren in de maphiërarchie of het zoeken naar een bepaald element op naam.

**Responsgrootte**

`searchAssets` keert tot 1000 activa in één enkele vraag terug. Om tot 10.000 activa per vraag terug te keren, beperk de reactiegegevens tot een ondergroep van `totalRows`, `name`, `handle`, `type`, en `subType` velden. Als u grotere sets wilt retourneren, stelt u paginering in met de `resultPage` parameter.

**Resultaatbestandsgrootte beperken met responseFieldArray of excludeFieldArray**

Beperk de grootte van de gegevensset met de `responseFieldArray` of `excludFieldArray` parameters. Deze parameters helpen geheugengebruik en bandbreedte te verminderen en kunnen de tijden van de serverreactie verbeteren.

## Geautoriseerde gebruikerstypen {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees toegang hebben om activa terug te keren.

## Parameters {#section-49aabc0600764f55a8b7017d86ded44f}

**Input (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Vereist? </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De handgreep aan het bedrijf met de activa u wilt zoeken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Hiermee kunnen beheerders als een andere gebruiker werken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Laat beheerders als deel van een verschillende groep werken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> map</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Het hoofdpad voor het zoeken naar elementen. Als deze wordt weggelaten, wordt de hoofdmap van het bedrijf gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4">Instellen op <span class="codeph"> true</span> naar submappen zoeken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> De keuze van de publicatiestatus. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> prullenbakState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4">Kies de status Prullenbak. Standaard is <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Keuze uit zoekmodi om de resultaten van <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>, en <span class="codeph"> metadataConditionArray</span>. Standaard is <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p> <p>Opmerking: Vervangen parameter. Het wordt aanbevolen het niet te gebruiken. </p> </p> <p>Een tekenreeks met overeenkomende trefwoorden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Keuze van zoekmodi om te combineren <span class="codeph"> systemFieldCondition</span> overeenkomsten. Standaard is <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> De array van systeemveldomstandigheden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4">Zoekmodi tekenreeksconstanten. De standaardwaarde is <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagConditionArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Een array met zoekvoorspelling van tagvelden. </p> <p>Voorspellen worden gecombineerd op basis van de <span class="codeph"> tagMatchMode</span> en vervolgens gecombineerd met termen in <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span>, en <span class="codeph"> metadataConditionArray</span> volgens de <span class="codeph"> conditionMatchMode</span> instellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4">Zoekmodi voor combineren <span class="codeph"> metadataCondition</span> overeenkomsten. Standaard is <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> De array met zoekvoorwaarden voor metagegevensvelden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Array met elementtypen die in de zoekopdracht moet worden opgenomen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Array met elementtypen die moeten worden uitgesloten van zoekopdracht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Een lijst met subtypenamen waarop u wilt filteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4">Indien <span class="codeph"> true</span> en <span class="codeph"> assetSubTypeArray</span> is niet leeg, alleen activa waarvan de subtypes in <span class="codeph"> assetSubTypeArray</span> worden geretourneerd. Indien <span class="codeph"> false</span> (standaardwaarde), worden vervolgens activa zonder gedefinieerd subtype geretourneerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Indien waar (true), worden bijproductelementen die worden gegenereerd tijdens de opname van een primair element, zoals afbeeldingen op pagina's met bijgesneden PDF, niet opgenomen in zoekresultaten. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Array met voorwaarden voor het genereren van byteproducten om elementen uit te sluiten van zoekresultaten. Indien aanwezig, treedt deze parameter de excludeByproducts die plaatsen met voeten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:posten</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Handle van een project dat de activa bevat aan onderzoek. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Maximumaantal resultaten dat moet worden geretourneerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4">Hiermee geeft u de resultatenpagina op die u wilt retourneren, op basis van <span class="codeph"> recordsPerPage</span> paginaformaat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Keuze van velden voor het sorteren van elementen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Keuze van sorteerrichting. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Bevat een lijst met velden en subvelden voor opname in de reactie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Bevat een lijst met velden en subvelden die kunnen worden uitgesloten van de reactie. </td> 
  </tr> 
 </tbody> 
</table>

**Uitvoer (searchAssetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| totalRows | `xsd:int` | Nee | Het aantal rijen dat een zoekopdracht retourneert wanneer records per pagina niet beperkt zijn. |
| assetArray | `types:AssetArray` | Nee | Elementen die de zoekopdracht retourneert. |

## Voorbeelden {#section-725484cc09b54772a838ad2cc930b94b}

In dit codevoorbeeld wordt gezocht naar afbeeldingselementen die bij een bepaald bedrijf horen. De reactie is afgebroken voor de beknoptheid.

**Verzoek**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Antwoord**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```
