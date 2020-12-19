---
description: vntc genereert tekstgegevens die naar stderr of het logbestand worden verzonden.
seo-description: vntc genereert tekstgegevens die naar stderr of het logbestand worden verzonden.
seo-title: Uitvoer
solution: Experience Manager
title: Uitvoer
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Uitvoer{#output}

vntc genereert tekstgegevens die naar stderr of het logbestand worden verzonden.

De gegevens worden opgemaakt als één `name=value` eigenschap per tekstrecord. Tekenreekswaarden worden niet vermeld. Waarschuwings- en foutberichten worden altijd naar `stderr` verzonden, zelfs als `-log` is opgegeven.

Bepaalde eigenschappen kunnen meerdere keren voorkomen in dezelfde uitvoer. Aan de naam van deze eigenschappen wordt een volgnummer, beginnend met 0, toegevoegd, gescheiden door een punt. Dergelijke eigenschappen worden hieronder geïdentificeerd met een `. *`n`*` achtervoegsel na de bezitsnaam.

De volgende eigenschappen worden gegenereerd:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>De RGB-achtergrondkleur van de stijl van het kabinet. Alleen stijlen voor kabinetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>De standaardversie van het uitvoerbestand. Ook het hoogste bestandsversienummer dat deze release van <span class="filepath"> vntc</span> kan genereren. </p></td> 
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
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 als de behuizing glazen deuren bevat, 0 in andere gevallen. Alleen stijlen voor kabinetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>De naam van iccProfile dat is ingesloten in het <span class="varname"> sourceFile</span>. </p> <p>Leeg als <span class="varname"> sourceFile</span> geen color-managed is. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Informatiebericht, zoals voortgangsinformatie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 als  <span class="varname"> </span> sourceFile een master vignet is, 0 als het eerder met  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span> is verwerkt. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 0 </span> als  <span class="varname"> </span> sourceFile een kabinetstijl is die JPEG-afbeeldingsgegevens bevat (in dit geval wordt ook een waarschuwing weergegeven), anders 1. Alleen kabinet en venster dat stijlbestanden bedekt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>De maximale geheugenlimiet die van toepassing is op het actieve <span class="filepath"> vntc</span>-proces. <span class="varname"> </span> stringis  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> of  <span class="codeph">  </span> 0(uitgeschakeld). Waarbij <span class="varname"> K</span>, <span class="varname"> M</span> en <span class="varname"> G</span> verwijzen naar Kilobytes (1024 bytes), Megabytes (1048576 bytes) en Gigabytes (1073741824 bytes) ). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Schaal van het laagste resolutie piramide niveau in het outputvignet. Alleen aanwezig als <span class="codeph"> -piramid</span> is opgegeven. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Het aantal materialen dat is opgeslagen in <span class="varname"> sourceFile</span>. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Het aantal paneelafbeeldingen in dit kabinetstijlbestand. Alleen stijlen voor kabinetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Het aantal piramideniveaus in het uitvoervignet. Alleen aanwezig als -piramide is opgegeven. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 als het bron- of doelvignet een piramidestructuur heeft. Alleen vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Voor kabinetstijlen, de objecten resolutie van <span class="varname"> sourceFile</span>. Voor vignetten, is dit de geadviseerde materiaalresolutie voor beste kwaliteit teruggeeft resultaten wanneer het teruggeven van het outputvignet. Pixels/inch (ppi). </p></td> 
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
  <td class="stentry"> <p>Het volledig gekwalificeerde <span class="varname"> sourceFile</span> pad. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>De bestandsversie van <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFile is een vignet,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFile is een kabinetstijl, of  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFile is een venster dat stijl bedekt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>De waarde die is opgegeven met <span class="codeph"> -version</span> of de waarde van<span class="codeph"> defaultFileVersion</span> als<span class="codeph"> -version</span> niet is opgegeven. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Een door komma's gescheiden lijst met de pixelgrootten van alle weergaven in het uitvoervignet (de weergave met volledige resolutie voor piramidevignetten), van de standaardpaneelafbeelding in een kabinetsstijlbestand of van de eerste dekkingsafbeelding van een vensterbedekkingsstijlbestand. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 als de kabinetstijl tekentabel is, 0 anders. Niet aanwezig voor vignetten en vensterbekledingsstijldossiers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">waarschuwing.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Waarschuwingsbericht (bijvoorbeeld wanneer <span class="codeph"> -imagemap</span> is opgegeven maar er geen kaartgegevens zijn gevonden in het vignet). </p></td> 
 </tr> 
</table>

