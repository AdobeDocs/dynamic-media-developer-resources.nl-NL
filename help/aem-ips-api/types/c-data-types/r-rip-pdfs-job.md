---
description: Een proces dat een bestaand PDF-element opnieuw negeert.
solution: Experience Manager
title: RipPdfsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

Een proces dat een bestaand PDF-element opnieuw negeert.

>[!NOTE]
>
>Dit taaktype is afgekeurd. Overgang naar `ReprocessAssetsJob` voor alle toekomstige integratie.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Verwerk de array met PDF-bestanden die moeten worden bijgesneden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Hiermee bepaalt u of u een masker wilt maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor handmatig uitsnijden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor automatisch uitsnijden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Een array met projecthandgrepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>E-mailinstellingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>De URL waarnaar de bestanden worden geüpload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Taakgegevens voor een publicatietaak die wordt uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Taakgegevens voor een publicatietaak voor het renderen van afbeeldingen die moet worden uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Taakgegevens voor een publicatietaak voor video die moet worden uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Adobe InDesign-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masker de achtergrond voor geselecteerde afbeeldingen. Hierdoor kunt u ze in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp. </p> <p>Optioneel. </p> <p>Zie<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Notities {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Keuzen voor `*CropOptions` omvatten:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Keuzen voor `*PublishJob` omvatten:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
