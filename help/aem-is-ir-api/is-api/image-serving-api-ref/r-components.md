---
description: 'Scène 7 Beeldserver bestaat uit de volgende componenten '
solution: Experience Manager
title: Onderdelen van Image Serving
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---


# Image Serving components{#image-serving-components}

Scène 7 Beeldserver bestaat uit de volgende componenten:

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
   <td colname="col2"> <p>Stand-alone uitvoerbaar verantwoordelijk voor aanvang, het tegenhouden, en het verzekeren van de gezondheid van de andere componenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Biedt de omgeving voor de meeste op Java gebaseerde componenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bewaking-/waarschuwingsservice </p> </td> 
   <td colname="col2"> <p>J2EE-toepassing. Biedt serverbewaking en e-mailwaarschuwingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Platform Server </p> </td> 
   <td colname="col2"> <p>J2EE-toepassing. Beheert cliëntverbindingen, registreren, mededelingen met andere componenten. HTTP-toegang op <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caching Service </p> </td> 
   <td colname="col2"> <p>J2EE-toepassing. Beheert de gegevenscache van de Platform Server. De toegang van HTTP bij /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afbeeldingsserver </p> </td> 
   <td colname="col2"> <p>Voert alle I/O-bewerkingen van afbeeldingsverwerking en afbeeldingsbestanden uit. Zowel 32-bits als 64-bits uitvoerbare bestanden zijn beschikbaar voor Linux (32-bits alleen voor Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE-tekstrendercomponent </p> </td> 
   <td colname="col2"> <p>Een of meer instanties van de service voor het renderen van tekst kunnen actief zijn wanneer bewerkingen <span class="codeph"> textPs=</span> worden uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG-rendercomponent </p> </td> 
   <td colname="col2"> <p>Zelfstandige Java-toepassing (niet gehost door Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media Image Rendering (ook bekend als) Server renderen) </p> </td> 
   <td colname="col2"> <p>Hiervoor is een aparte licentie vereist. HTTP-toegang op <span class="filepath"> /ir/render</span>. Alle het Teruggeven van het Beeld functionaliteit is geïntegreerd in de Server van het Platform en de Server van het Beeld, zonder afzonderlijke uitvoerbare componenten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Aanvullende configuratie-instellingen worden verschaft door de standaardcatalogus ( [!DNL default.ini]) of specifieke afbeeldingscatalogi (zie [Afbeeldingscatalogi](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) voor meer informatie).
