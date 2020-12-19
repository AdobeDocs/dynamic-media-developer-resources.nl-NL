---
description: Hulpprogramma voor het valideren van afbeeldingen. Dit opdrachtregelhulpprogramma controleert afbeeldingsbestanden om te controleren of deze geldig zijn en zonder problemen kunnen worden gelezen door Image Serving.
seo-description: Hulpprogramma voor het valideren van afbeeldingen. Dit opdrachtregelhulpprogramma controleert afbeeldingsbestanden om te controleren of deze geldig zijn en zonder problemen kunnen worden gelezen door Image Serving.
seo-title: validate
solution: Experience Manager
title: validate
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# validate{#validate}

Hulpprogramma voor het valideren van afbeeldingen. Dit opdrachtregelhulpprogramma controleert afbeeldingsbestanden om te controleren of deze geldig zijn en zonder problemen kunnen worden gelezen door Image Serving.

Alle niet-PTIFF-afbeeldingsbestanden moeten worden gevalideerd voordat het bestand beschikbaar wordt gemaakt voor afbeeldingen die als bronafbeelding fungeren. PTIFF-afbeeldingen moeten worden gevalideerd na mogelijk onbetrouwbare kopieerbewerkingen.

## Gebruik {#usage}

` validate *``* [ *``*] [ *`fileTypeoptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -alle  </span> </p> <p>bronbestandstype; er moet ten minste één worden opgegeven (-om staat dezelfde afbeeldingsbestandstypen toe die worden ondersteund door IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opties  </span> </span> </p> </td> 
  <td class="stentry"> <p>Andere opdrachtopties (zie hieronder). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> Afbeeldingsbestand. Geen of meer, gescheiden door spaties. </p> </td> 
 </tr> 
</table>

## Retourneert {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 indien gelukt. Als een fout optreedt, wordt een waarde die niet gelijk is aan nul geretourneerd en worden foutgegevens verzonden naar `stderr`.

## Opties {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee geeft u een afzonderlijk tekstbestand op dat de lijst met afbeeldingsbestanden bevat. Eén record per bestand. Als <span class="codeph"> -fileList </span> is opgenomen, moet <span class="varname"> sourceFile </span> niet worden opgegeven. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>Hiermee schakelt u verificatie van het gehele afbeeldingsbestand in. Standaard wordt alleen de koptekst van de afbeelding gevalideerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>Hiermee wordt gecontroleerd of het ingesloten kleurprofiel geldig is. Standaard is de hoofdtekst van het profiel niet ingeschakeld. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -weiger16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> Hiermee worden afbeeldingen met 16 bits per afbeeldingscomponent afgewezen. Altijd opgegeven door de afbeeldingsserver wanneer externe bronafbeeldingen worden gevalideerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> Hiermee wordt meer informatie afgedrukt als de afbeelding ongeldig is. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p>Schakelt <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> uitvoer uit. Alleen een status wordt geretourneerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>Beëindigt verwerking wanneer een fout van de dossierbevestiging voorkomt, zelfs als de extra dossiers nog moeten worden bevestigd. De verwerking gaat standaard door wanneer een validatiefout optreedt </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  </span> </p> </td> 
  <td class="stentry"> <p>Retourneert versiegegevens voor dit hulpprogramma. Opgeven zonder andere opties. </p> </td> 
 </tr> 
</table>

