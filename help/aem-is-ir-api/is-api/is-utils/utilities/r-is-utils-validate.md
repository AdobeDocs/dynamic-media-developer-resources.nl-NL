---
description: Hulpprogramma voor het valideren van afbeeldingen. Dit opdrachtregelprogramma controleert afbeeldingsbestanden om er zeker van te zijn dat deze geldig zijn en dat de Image Serving ze zonder problemen kan lezen.
solution: Experience Manager
title: validate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# validate{#validate}

Hulpprogramma voor het valideren van afbeeldingen. Dit opdrachtregelprogramma controleert afbeeldingsbestanden om te controleren of deze geldig zijn en zonder problemen kunnen worden gelezen door Image Serving.

Alle niet-PTIFF-afbeeldingsbestanden moeten worden gevalideerd voordat het bestand beschikbaar wordt gemaakt voor de afbeelding die als bronafbeelding fungeert. PTIFF-afbeeldingen moeten worden gevalideerd na mogelijk onbetrouwbare kopieerbewerkingen.

## Gebruik {#usage}

` validate *`fileType`* [ *`opties`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Bronbestandstype; ten minste één bestandstype moet worden opgegeven (-een staat dezelfde afbeeldingsbestandstypen toe die worden ondersteund door IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opties </span> </span> </p> </td> 
  <td class="stentry"> <p>Andere opdrachtopties (zie verderop). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Afbeeldingsbestand. Geen of meer, gescheiden door spaties. </p> </td> 
 </tr> 
</table>

## Retourneert {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 indien gelukt. Als er een fout optreedt, wordt een andere waarde dan nul geretourneerd en worden foutgegevens verzonden naar `stderr`.

## Opties {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee geeft u een afzonderlijk tekstbestand op dat de lijst met afbeeldingsbestanden bevat. Eén record per bestand. Indien <span class="codeph"> -fileList </span> is opgenomen, <span class="varname"> sourceFile </span> mag niet worden opgegeven. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Hiermee schakelt u verificatie van het gehele afbeeldingsbestand in. Standaard wordt alleen de koptekst van de afbeelding gevalideerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Hiermee wordt gecontroleerd of het ingesloten kleurprofiel geldig is. Het hoofdtekstprofiel wordt standaard niet gecontroleerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -weiger16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Hiermee worden afbeeldingen met 16 bits per afbeeldingscomponent afgewezen. Altijd opgegeven door de afbeeldingsserver wanneer externe bronafbeeldingen worden gevalideerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Hiermee wordt meer informatie afgedrukt als de afbeelding ongeldig is. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>Uitschakelen <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> uitvoer. Alleen een status wordt geretourneerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Beëindigt verwerking wanneer een fout van de dossierbevestiging voorkomt, zelfs als de extra dossiers nog moeten worden bevestigd. De verwerking gaat standaard door wanneer een validatiefout optreedt </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Retourneert versiegegevens voor dit hulpprogramma. Opgeven zonder andere opties. </p> </td> 
 </tr> 
</table>
