---
description: De standaardalarm wordt verzonden met een geconsolideerd e-mailbericht aan het eind van het gevormde gemiddelde interval.
seo-description: De standaardalarm wordt verzonden met een geconsolideerd e-mailbericht aan het eind van het gevormde gemiddelde interval.
seo-title: Standaardwaarschuwingen
solution: Experience Manager
title: Standaardwaarschuwingen
topic: Scene7 Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---


# Standaardwaarschuwingen{#standard-alerts}

De standaardalarm wordt verzonden met een geconsolideerd e-mailbericht aan het eind van het gevormde gemiddelde interval.

In de volgende tabel wordt elk type standaardwaarschuwing beschreven.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Type waarschuwing</b> </th> 
   <th class="entry"> <b>Titel-id</b> </th> 
   <th class="entry"> <b>Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Vergrendeld verzoek </p> </td> 
   <td> <p>Vergrendelen </p> </td> 
   <td> <p>Verzonden wanneer een verzoek er niet in slaagt een reactie op de client binnen de opgegeven drempel te retourneren. Dit kan wijzen op hangende verzoeken, die kunnen leiden tot uitputting van de Java thread pool. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Hoog gelijktijdig </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Wordt verzonden wanneer het aantal aanvragen dat gelijktijdig wordt verwerkt (de <i>overlapping</i>) de opgegeven drempel overschrijdt. Kan wijzen op een overbelastingsvoorwaarde voor de server. </td> 
  </tr> 
  <tr> 
   <td> <p>Minimumverkeer </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Gegenereerd wanneer het totale verzoektarief onder de gespecificeerde drempel daalt. Dit geeft doorgaans een probleem met servercommunicatie aan (bijvoorbeeld wanneer een server offline wordt gezet). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Foutfrequentie </p> </td> 
   <td> <p>Fout </p> </td> 
   <td> <p>Wordt verzonden wanneer de gemiddelde frequentie van HTTP-foutreacties tijdens het samplinginterval de opgegeven drempel overschrijdt. Dit kan wijzen op configuratieproblemen, ontbrekende afbeeldingen of fouten met betrekking tot het programmeren van websites of databases. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Responstijd </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Wordt verzonden wanneer de gemiddelde verwerkingstijd van de aanvraag tijdens het bemonsteringsinterval boven de opgegeven drempel uitkomt. Geeft doorgaans een tijdelijke of blijvende overbelastingsvoorwaarde van de server of het back-end afbeeldingsopslagsysteem aan. </p> <p>De reacties van de fout worden niet in aanmerking genomen wanneer het berekenen van de gemiddelde reactietijd. </p> </td> 
  </tr> 
 </tbody> 
</table>

