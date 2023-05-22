---
description: vntc genereert tekstgegevens die naar stderr of het logbestand worden verzonden.
solution: Experience Manager
title: Uitvoer
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Uitvoer{#output}

vntc genereert tekstgegevens die naar stderr of het logbestand worden verzonden.

De gegevens worden als één bestand opgemaakt `name=value` eigenschap per tekstrecord. Tekenreekswaarden worden niet vermeld. Waarschuwing en foutberichten worden altijd verzonden naar `stderr`, zelfs als `-log` wordt opgegeven.

Bepaalde eigenschappen kunnen meerdere keren voorkomen in dezelfde uitvoer. Aan de naam van deze eigenschappen wordt een volgnummer, beginnend met 0, toegevoegd, gescheiden door een punt. Dergelijke eigenschappen worden hieronder aangeduid met een `. *`n`*` achtervoegsel achter de naam van de eigenschap.

De volgende eigenschappen worden gegenereerd:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ivaal</span>,<span class="varname"> ivaal</span>,<span class="varname"> ivaal</span></span> </p> </td> 
  <td class="stentry"> <p>De RGB-achtergrondkleur van de kast. Alleen stijlen voor kabinetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>De standaardversie van het uitvoerbestand. Ook het hoogste bestandsversienummer van deze versie van <span class="filepath"> vntc</span> kan genereren. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">fout.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Foutbericht. De aanwezigheid van foutberichten geeft doorgaans aan dat er geen uitvoerbestand(en) zijn gemaakt of dat deze niet geschikt zijn voor gebruik door het renderen van afbeeldingen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bestand.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Het volledig gekwalificeerde pad/de naam van alle uitvoerbestanden, inclusief vignetten, bestanden met de stijl van het kabinet, afbeeldingen met volledige resolutie en miniaturen. Er is één bestandskenmerk aanwezig voor elk gegenereerd bestand (behalve het logbestand). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glas=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ivaal</span> 1 als de behuizing glazen deuren bevat, 0 in andere gevallen. Alleen stijlen voor kabinetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>De naam van het ingesloten profiel iccProfile in het dialoogvenster <span class="varname"> sourceFile</span>. </p> <p>Leeg als <span class="varname"> sourceFile</span> is geen kleurbeheer. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Informatiebericht, zoals voortgangsinformatie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ivaal</span> is 1 als <span class="varname"> sourceFile</span> is een master vignet, 0 als het eerder is verwerkt met <span class="filepath"> vnUpdate</span> of <span class="filepath"> vntc</span>. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ivaal</span> is 0 als <span class="varname"> sourceFile</span> is een kabinetstijl met JPEG-afbeeldingsgegevens (in dit geval wordt ook een waarschuwing weergegeven), in andere gevallen 1. Alleen kabinet en venster dat stijlbestanden bedekt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>De maximale geheugenlimiet die van toepassing is op de uitvoering <span class="filepath"> vntc</span> proces. <span class="varname"> string</span> is ofwel <span class="varname"> ivaal</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span>, of <span class="codeph"> 0</span> (uitgeschakeld). Wanneer <span class="varname"> K</span>, <span class="varname"> M</span>, en <span class="varname"> G</span> verwijzen naar Kilobytes (1024 bytes), Megabytes (1048576 bytes) en gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>Schaal van het laagste resolutie piramide niveau in het outputvignet. Alleen presenteren als <span class="codeph"> -piramide</span> wordt opgegeven. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>Het aantal materialen dat is opgeslagen in het dialoogvenster <span class="varname"> sourceFile</span>. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>Het aantal paneelafbeeldingen in dit kabinetstijlbestand. Alleen stijlen voor kabinetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>Het aantal piramideniveaus in het uitvoervignet. Alleen aanwezig als -piramide is opgegeven. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramide=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>0 als het bron- of doelvignet een piramidestructuur heeft. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolutie=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Voor kabinetstijlen, de objectresolutie van het<span class="varname"> sourceFile</span>. Voor vignetten, is dit de geadviseerde materiaalresolutie voor beste kwaliteit teruggeeft resultaten wanneer het teruggeven van het outputvignet. Pixels/inch (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>De kleinste objectresolutie in het uitvoervignet. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>De gemiddelde objectresolutie in het uitvoervignet. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>De volledig gekwalificeerde <span class="varname"> sourceFile</span> pad. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>De bestandsversie van <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ivaal</span>,<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>De pixelgrootte van het invoervignet, de standaardpaneelafbeelding in een kabinetsstijlbestand of de eerste dekkingsafbeelding van een vensterbedekkend stijlbestand. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Het type vensterbedekking (alleen voor vensterbedekkende stijlen): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=horizontale schaduw of zonwering </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=verticale zonwering </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=korte gordijnen met volledige breedte </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=korte afvoer links/rechts </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=volledig-breedte volledig-lengtegordijnen </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=links/rechts, volledige-lengteschakelingen </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=cafégordijn </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valentie </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> indien <span class="varname"> sourceFile</span> een vignet is, <span class="codeph"> vnc</span> indien <span class="varname"> sourceFile</span> een kabinetstijl is, of <span class="codeph"> vnw</span> indien <span class="varname"> sourceFile</span> is een vensterbedekkende stijl. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>De waarde die is opgegeven met <span class="codeph"> -version</span>of de waarde van<span class="codeph"> defaultFileVersion</span> indien<span class="codeph"> -version</span> is niet opgegeven. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ivaal</span>,<span class="varname"> ivaal</span>*[,<span class="varname"> ivaal</span>,<span class="varname"> ivaal</span>]</span> </p></td> 
  <td class="stentry"> <p>Een door komma's gescheiden lijst met de pixelgrootten van alle weergaven in het uitvoervignet (de weergave met volledige resolutie voor piramidevignetten), van de standaardpaneelafbeelding in een kabinetsstijlbestand of van de eerste dekkingsafbeelding van een vensterbedekkingsstijlbestand. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ivaal</span> is 1 als de kabinetstijl tekentabel is, anders 0. Niet aanwezig voor vignetten en vensterbekledingsstijldossiers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">waarschuwing.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Waarschuwingsbericht (bijvoorbeeld wanneer <span class="codeph"> -imagemap</span> wordt opgegeven, maar er worden geen kaartgegevens gevonden in het vignet). </p></td> 
 </tr> 
</table>
