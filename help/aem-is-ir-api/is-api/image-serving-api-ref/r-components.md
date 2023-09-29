---
title: Onderdelen van Image Serving
description: Dynamic Media Image Serving bestaat uit de volgende onderdelen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Onderdelen van Image Serving{#image-serving-components}

Dynamic Media Image Serving bestaat uit de volgende onderdelen:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Servertoezichthouder </p> </td> 
   <td colname="col2"> <p>Een zelfstandig uitvoerbaar bestand dat verantwoordelijk is voor het starten, stoppen en controleren van de gezondheid van de andere componenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Het biedt de omgeving voor de meeste Java-componenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bewaking-/waarschuwingsservice </p> </td> 
   <td colname="col2"> <p>J2EE-toepassing. Biedt serverbewaking en e-mailwaarschuwingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE-toepassing. Beheert cliëntverbindingen, registreren, mededelingen met andere componenten. HTTP-toegang op <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caching Service </p> </td> 
   <td colname="col2"> <p>J2EE-toepassing. Beheert de [!DNL Platform Server]Gegevens cache. De toegang van HTTP bij /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afbeeldingsserver </p> </td> 
   <td colname="col2"> <p>Hierbij worden alle I/O-bewerkingen op het gebied van beeldverwerking en afbeeldingsbestanden uitgevoerd. Zowel 32-bits als 64-bits uitvoerbare bestanden zijn beschikbaar voor Linux® (32-bits alleen voor Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE-tekstrendercomponent </p> </td> 
   <td colname="col2"> <p>Een of meer instanties van de service voor het renderen van tekst kunnen actief zijn wanneer <span class="codeph"> textPs=</span> bewerkingen worden uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG Rendercomponent </p> </td> 
   <td colname="col2"> <p>Zelfstandige Java™-toepassing (niet gehost door Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media Image Rendering (ook bekend als) Server renderen) </p> </td> 
   <td colname="col2"> <p>Hiervoor is een aparte licentie vereist om te activeren. HTTP-toegang op <span class="filepath"> /ir/render</span>. Alle functies voor het renderen van afbeeldingen zijn geïntegreerd in de [!DNL Platform Server] en de Server van het Beeld, zonder afzonderlijke uitvoerbare componenten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Aanvullende configuratie-instellingen worden verschaft door de standaardcatalogus ( [!DNL default.ini]) of specifieke afbeeldingscatalogi (zie [Afbeeldingscatalogi](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) voor meer informatie).
