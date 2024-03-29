---
title: Sessiecatalogus
description: De zittingscatalogus is de materiaalcatalogus die zittingsattributen voor het verzoek, en een standaardwaarde catId voor al src=, vignette=, en icc= bevelen verstrekt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Sessiecatalogus{#session-catalog}

De sessiecatalogus is de materiaalcatalogus met sessiekenmerken voor de aanvraag en een standaard catId-waarde voor alle `src=`, `vignette=`, en `icc=` opdrachten.

De sessiecatalogus wordt opgegeven als het eerste padelement van het HTTP-aanvraagpad (direct na de servernaam). Als het eerste padelement niet overeenkomt met kenmerk:RootId van een catalogus, wordt de standaardcatalogus gebruikt als een sessiecatalogus.

De sessiecatalogus bevat de volgende standaardwaarden voor sessies:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Kenmerk </p> </th> 
   <th class="entry"> <p>Notities </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::RootPath</span> </p> </td> 
   <td> <p> Hoofdpad voor materiaalgegevensbestanden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk:VignetPath</span> </p> </td> 
   <td> <p> Hoofdpad voor vignetbestanden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::IccProfileRgb</span> </p> </td> 
   <td> <p> Standaardwerkkleurruimte als een vignet geen ICC-profiel insluit </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk:RootUrl</span> </p> </td> 
   <td> <p> URL van hoofdmap voor relatieve HTTP-bestandspaden in <span class="codeph"> src=</span> opdrachten </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Oorspronkelijke tonen/verbergen-status voor overlappende objecten </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::Expiration</span> </p> </td> 
   <td> <p> Tijd-aan-levende waarde van het antwoordbeeld voor volmachtsserver en browser geheime voorgeheugens </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::MaxPix</span> </p> </td> 
   <td> <p> De maximaal toegestane breedte en hoogte van de antwoordafbeelding </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::DefaultPix</span> </p> </td> 
   <td> <p> Standaardwaarden voor <span class="codeph"> wid=</span> en <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::Format</span> </p> </td> 
   <td> <p> Standaardwaarde voor <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk:JpegQuality</span> </p> </td> 
   <td> <p> Standaardwaarde voor <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::TiffEncoding</span> </p> </td> 
   <td> <p> Compressietype voor uitvoer van TIFF-afbeelding </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk:Verscherpen</span> </p> </td> 
   <td> <p> Standaardwaarde voor <span class="codeph"> scherpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::OnFailSel</span> </p> </td> 
   <td> <p> Hiermee wordt gedrag opgegeven wanneer een <span class="codeph"> sel=</span> opdracht mislukt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::OnFailObj</span> </p> </td> 
   <td> <p> Hiermee wordt gedrag opgegeven wanneer een <span class="codeph"> obj=</span> opdracht mislukt </p> </td> 
  </tr> 
 </tbody> 
</table>
