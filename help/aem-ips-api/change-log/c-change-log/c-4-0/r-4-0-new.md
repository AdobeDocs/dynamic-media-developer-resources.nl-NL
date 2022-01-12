---
title: Nieuwe toevoegingen en wijzigingen
description: Beschrijft nieuwe en uitgevoerde veranderingen voor IPS API v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 0%

---

# Nieuwe toevoegingen en wijzigingen{#new-additions-and-changes}

Beschrijft nieuwe en uitgevoerde veranderingen voor IPS API v4.0.

Geïmplementeerd naast-zij API versies met afzonderlijke WSDLs en schema namespaces.

* Vorige API-versies: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versie SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Toegevoegd `PostScriptOptions/alpha` veld.

Toegevoegd `VideoRootUrl` en `SwfRootUrl` eigenschappen voor `getProperty` bewerking.

Optioneel toegevoegd `appName` en `appVersion` param naar `authHeader` om de aanroepende toepassing bij te houden. Toegevoegde logboekregistratie aan `ipsApiService.log`.

Optioneel toegevoegd `serviceUrl` param aan de WSDL generatieservlet. Deze param is nuttig voor zuivert volmachten. Bijvoorbeeld: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Geïmplementeerd `getZipEntries` bewerking.

Geïmplementeerde zoekbereiken en getypte vergelijkingswaarden voor systeemveldomstandigheden.

Toegevoegd `'Asset'` Tekenreeksconstante voor het type element, voornamelijk om metagegevensvelden tussen elementen toe te staan.

Geïmplementeerd `trashState` param for `searchAssets`.

Geïmplementeerd `getAssetPublishHistory` bewerking.

Optioneel toegevoegd `faultHttpStatusCode` SOAP-koptekst om foutafhandeling in Flex mogelijk te maken. Gebruik voor Flex `<faultHttpStatusCode>200</faultHttpStatusCode>`. De standaardstatuscode voor foutreacties is `500 (Internal Server Error)`.

Toegevoegde bewerkingen om elementen uit de prullenbak en lege elementen uit de prullenbak te herstellen.

Geïmplementeerde CRUD-bewerkingen.

Toegevoegde ingeschakelde markering aan `ImageMap` type en `saveImageMap` bewerking.

Toegevoegde ondersteuning voor de taken Resterende bestanden optimaliseren.

Toegevoegd `setAssetsPublishState` voor bulksgewijze updates van publicatiestatus.

Toegevoegd `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Vervangen `saveMetadataField` operatie ten gunste van nieuwe `createMetadataField` en `updateMetadataField` bewerkingen.

Geïmplementeerd `deleteAssetsParam` batch-verwijderbewerking.

Geïmplementeerd `moveAssetsParam` batch-verplaatsingsbewerking.

Geïmplementeerd `deleteMetadataField` bewerking.

Geïmplementeerd `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` bewerkingen.

Geïmplementeerd `getAssetCounts`.

Extra ondersteuning voor `setImageSetMembers` voor `RenderSet` leden in `ImageSet` activa.

Toegevoegd `replaceImage` bewerking.

Toegevoegd `copyImage` bewerking.

Toegevoegd `setUrlModifier` de werking en `urlModifier/urlPostApplyModifier` velden voor `LayerViewInfo`, `TemplateInfo`, en `WatermarkInfo`.

Toegevoegd `createDerivedAsset` bewerking. Momenteel worden de `ownerHandle` moet verwijzen naar een afbeeldingselement en het type mag `AdjustedView` of `LayerView`.

Toegevoegd `createTemplate` bewerking. Aanroep om sjabloon- of watermerkelementen te maken.

IPS-bedrijfsinstellingen, `CompanySettings`, die naar de webservices-API is verzonden.

Toegevoegd `excludeByproducts` filtervlag naar `searchAssets` bewerking. Deze vlag instellen op ware runtimes `PSDlayer` afbeeldingen en afbeeldingen met PDF.

Toegevoegd `getGenerationInfo` bewerking.

Toegevoegd `SystemMessage` eigenschapsnaam naar `getProperty` bewerking.

Bepaalde tekenreeksconstanten voor het type element zijn gewijzigd zodat deze overeenkomen met de corresponderende velden voor Asset Info.

* WordDoc: Woord
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Gewijzigde resultaatindeling van batchbewerkingen als overzicht van succes, waarschuwingen en fouten.

Geïmplementeerd `batchSetAssetMetadata` batch-metagegevensbewerking.

Geïmplementeerde ondersteuning voor toepassingsspecifieke gegevens.

Geïmplementeerde ondersteuning voor booleaanse vlaggen voor `createTemplate`, `extendLayers`, en `extractText` voor uploadtaken om het proces van Photoshop-verwerking te beheren (vergelijkbaar met wijzigingen voor het uploaden van bestanden).

Geïmplementeerd `setImageMaps` en `setZoomTargets` bewerkingen.

Geïmplementeerd `ViewerPreset` bewerkingen. De herkende typen zijn:

* `VideoPlayer` (Video publiceert alleen deze viewers.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

De skins van de viewer ondersteunen twee parameters: `skinFg` en `skinBg`. De achtergrondcode voert alle verwerking uit die wordt vereist om achterwaartse verenigbaarheid te handhaven.

Geïmplementeerd `getAssociatedAssets` bewerking.

Toegevoegd `ReprocessAssets` taaktype om eerder geüploade primaire bronbestanden opnieuw te kunnen verwerken, inclusief het terugzetten van PDF en het opnieuw optimaliseren van afbeeldingen.

Naam gewijzigd `PropertySetType` veldtype naar `propertyType`. Deze naam heeft invloed op de `createPropertySetType` parameter en `getPropertySetType/getPropertySetTypes` reactie.

Geïmplementeerd `batchSetImageFields` bewerking voor het instellen van afbeeldingsgebruikersgegevens en andere bewerkbare afbeeldingsvelden.

47 Het veld FileSize is toegevoegd aan verschillende elementgegevenstypen:

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Geïmplementeerd `getActivePublishContexts` bewerking. Deze bewerking retourneert een array met namen van publicatiecontext met actieve publicatieservers voor het opgegeven bedrijf. Huidige namen van publicatiecontext zijn:

* `ImageServing`
* `ImageRendering`
* `Video`

Geïmplementeerd `getSearchStrings` bewerking. Er wordt een array met zoektekenreeksen voor het opgegeven element geretourneerd.

Toegevoegde landinstellingsparameters voor taken en een mechanisme om de landinstelling voor API-bewerkingen in te stellen. De tekenreeks locale moet worden opgemaakt als `<language_code>[-<country_code>]`. De taalcode is een code in kleine letters, met twee letters zoals gespecificeerd in ISO-639, en de optionele landcode is een code in hoofdletters, met twee letters zoals gespecificeerd in ISO-3166.

Optionele parameter locale toegevoegd aan de `authHeader` SOAP-koptekst om de landinstelling voor API-bewerkingen in te stellen. Wanneer deze parameter niet aanwezig is, wordt de HTTP-header `Accept-Language` wordt gebruikt. Als deze kopbal ook niet aanwezig is, wordt de standaardscène voor de IPS server gebruikt.

Ondersteuning voor get/set toegevoegd voor metagegevensvelden met veel typen.

Implemented SOAP en HTTP header support for gzip response control.

Toegevoegd `gzipResponse` markeren naar `authHeader`. Als deze niet aanwezig is, controleert de API de HTTP `Accept-Encoding` header.

Toegevoegde ondersteuning voor searchAssets voor veldomstandigheden met sterk getypte metagegevens.

* Voor alle veldtypen kan de waarde worden doorgegeven met een tekenreeksvergelijkingsoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Voor Booleaanse velden: `boolVal` kan met de `Equals` op.
* Voor Int-velden, `longVal` kan worden doorgegeven met een numerieke vergelijkingsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) of `minLong/maxLong` kan worden doorgegeven met een numeriek bereik ( `Between, NotBetween`).
* Voor zwevende velden, `doubleVal` kan worden doorgegeven met een numerieke vergelijkingsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) of `minDouble/maxDouble` kan worden doorgegeven met een numeriek bereik ( `Between, NotBetween`).
* Voor Datumvelden kunt u doorgeven `dateVal` met een numerieke vergelijkingsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) of u kunt minDate/maxDate doorgeven met een numeriek bereik ( `Between, NotBetween`).

Toegevoegde beschrijving, `jobSubType`, en `originalJobName` velden naar `JobLog` type.

* `originalJobName` is de taaknaam die is ingediend bij `submitJob` (zonder unieke achtervoegsels of vervolgtaaknamen).
* `jobSubType` wordt alleen gebruikt door `ImageServingPublishJob` banen (waarbij `full`, `increment, fullwithsearch,` of `fulloverride`).
* `description` is een lege tekenreeks voor alle taaktypen, maar bevat uiteindelijk beknopte taakgegevens, zoals het uploadpad.

Bovendien worden de volgende velden niet in beide opgenomen `getJobLogs` en `getJobLogDetails`. In eerdere versies waren ze alleen beschikbaar met `getJobLogDetails`.

* `endDate` (als de taak is voltooid).
* `fileDuplicateCount` (voorheen was het altijd `0` with `getJobLogs`)
* `fileUpdateCount` (voorheen was altijd `0` with `getJobLogs` en opgenomen in `fileSuccessCount`; het is nu opgesplitst in afzonderlijke velden ) .

Veld assetHandle toegevoegd aan `JobLogDetail` type.

Optionele beschrijvingsparameter toegevoegd aan `submitJob`. Deze parameter wordt doorgegeven voor ophalen in `getScheduledJobs`, `getActiveJobs`, en `getJobLogs`.

Vervangen het SKU-systeemveld. Het veld wordt genegeerd als het wordt doorgegeven als een `SystemFieldCondition` tot `searchAssets`.

Toegevoegd `excludeAssetTypeArray` filteren naar `searchAssets`.

Toegevoegd `MaskInfo` tekst naar `Asset`.

Toegevoegde nieuwe Types van Activa voor beheer door IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Type element </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator-bestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS- en PostScript-bestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Word-document voor bestanden die eindigen met .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Excel-document voor bestanden die eindigen met .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® PowerPoint-document voor bestanden die eindigen met .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>RTF-bestand voor geüploade bestanden die eindigen met .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Extra opties toegevoegd aan `UploadDirectoryJob` en `UploadUrlsJob` om de verwerking van Postscript-, Illustrator- en PDF-bestanden onafhankelijk te beheren. Alle bestaande banen verstrekken de noodzakelijke parameters aan elk van de drie verwerkingspijpleidingen zodat zij precies functioneren zoals vandaag gebeurt. Het origineel `PostScriptOptions` wordt gebruikt om de verwerking voor Illustrator- en EPS/PS-bestanden in te stellen. Optioneel kunnen specifieke blokken met bestandsopties worden opgegeven om de verwerking op te geven. De lijst met wijzigingen bevat:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Veld </p> </th> 
   <th colname="col2" class="entry"> <p>Parameter </p> </th> 
   <th colname="col3" class="entry"> <p>Waarde </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proces </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Geen </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasteren </span>(standaard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Beheer alleen het actief en maak tijdens het uploaden geen derivaten. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Render het EPS- en PostScript-bestand naar een afbeelding met de opgegeven resolutie en kleurruimte. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optioneel. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Wordt gebruikt wanneer het bestand in een afbeelding wordt gerasterd. Er wordt een transparante achtergrond gemaakt als het oorspronkelijke bestand op deze manier is gedefinieerd voor het bedekken van logo's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proces </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Geen </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasteren </span> (standaard) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Beheer alleen het actief en maak tijdens het uploaden geen derivaten. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Render het bestand naar een afbeelding met de opgegeven resolutie en kleurruimte. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolutie </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Resolutie omzetten in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> kleurruimte </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Doelkleurruimte voor rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optioneel. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Wordt gebruikt wanneer het bestand in een afbeelding wordt gerasterd. Hiermee maakt u een transparante achtergrond als het oorspronkelijke bestand op deze manier is gedefinieerd voor het maken van bedekkende logo's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proces </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Geen </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasteren </span> (standaard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Beheer alleen het actief en maak tijdens het uploaden geen derivaten. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Render het bestand naar een afbeelding met de opgegeven resolutie en kleurruimte. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolutie </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Resolutie omzetten in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> kleurruimte </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Doelkleurruimte voor rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definieert of een PDF van meerdere pagina's na het renderen in een eCatalog moet worden gecombineerd (de standaardwaarde is true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Bepaalt of de woorden van de PDF in DB voor recentere levering aan een onderzoeksserver worden gehaald (gebrek is vals). </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt ook een query uitvoeren vanuit `getScheduledJobs`.

Gewijzigd `webservice.gzip.response` configuratie-eigenschap om een van de volgende waarden te gebruiken:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Waarde </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nooit </span> </p> </td> 
   <td colname="col2"> <p>Geen gzip respons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zeep </span> </p> </td> 
   <td colname="col2"> <p>Gzip-reactie alleen als authHeader/gzipResponse true is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accepteren </span> </p> </td> 
   <td colname="col2"> <p>Gzip als authHeader/gzipResponse waar is, of er geen gzipResponse-header aanwezig is en de HTTP Accept-Encoding-header gzip bevat. (Standaard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altijd </span> </p> </td> 
   <td colname="col2"> <p>Gzip altijd reactie, ongeacht headerwaarden. Gebruik deze waarde alleen voor foutopsporingsdoeleinden. </p> </td> 
  </tr> 
 </tbody> 
</table>
