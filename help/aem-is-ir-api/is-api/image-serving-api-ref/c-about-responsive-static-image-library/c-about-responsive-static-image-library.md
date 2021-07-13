---
description: Responsieve afbeeldingsbibliotheek is een JavaScript-module waarmee de kwaliteit van afbeeldingen die vanuit Dynamic Media worden aangeboden en die worden ingesloten in responsieve webpagina's, dynamisch wordt aangepast. Bovendien biedt de klasse een verbeterde beeldkwaliteit op apparaten met schermen met hoge dichtheid. De bibliotheek kan ook responsief resultaten renderen van Slim uitsnijden en Slim staal.
solution: Experience Manager
title: De bibliotheek met responsieve afbeeldingen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# De bibliotheek met responsieve afbeeldingen{#about-responsive-image-library}

Responsieve afbeeldingsbibliotheek is een JavaScript-module waarmee de kwaliteit van afbeeldingen die vanuit Dynamic Media worden aangeboden en die worden ingesloten in responsieve webpagina&#39;s, dynamisch wordt aangepast. Bovendien biedt de klasse een verbeterde beeldkwaliteit op apparaten met schermen met hoge dichtheid. De bibliotheek kan ook responsief resultaten renderen van Slim uitsnijden en Slim staal.

## Demo-URL&#39;s {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Het eenvoudigste gebruik van de bibliotheek met responsieve afbeeldingen is het definiëren van een lijst met onderbrekingspuntwaarden voor de afbeeldingsbreedte. Deze lijst zorgt ervoor dat de juiste vertoning wordt geladen en weergegeven wanneer de grootte van een afbeelding wordt gewijzigd omdat de webpaginalay-out is gewijzigd doordat de gebruiker het browservenster vergroot of verkleint of de richting van het apparaat wijzigt. De bibliotheek controleert voortdurend de afbeeldingsgrootte op het scherm en elke keer dat een nieuwe breedte voor een onderbrekingspunt wordt bereikt, wordt een nieuwe afbeeldingsuitvoering opgehaald uit Dynamic Media.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Demo-URL </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>In het volgende voorbeeld ziet u hoe de responsieve afbeelding zich in een container bevindt die 50% van de breedte van de webpagina in beslag neemt. Telkens wanneer de grootte van het browservenster wordt gewijzigd, verandert de breedte van de container. Wanneer de afbeeldingsbreedte een van de geconfigureerde onderbrekingspunten bereikt, die voor illustratieve doeleinden zijn ingesteld op 200, 400, 600 en 800 pixels, wordt een nieuwe uitvoering gedownload en weergegeven. Het doel is het laden van onnodige grote afbeeldingen te voorkomen en netwerkbandbreedte te besparen. </p> <p>Klik URL zodat opent u de Web-pagina, resize het browser venster, en controleert netwerkverkeer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>In het volgende Bootstrap-voorbeeld wordt hetzelfde gebruiksgeval in een webpagina getoond. Volgens Bootstrap CSS kan de lay-outcel waaraan de responsieve afbeelding wordt toegevoegd, een van de volgende breedten hebben: 360, 720 en 940 pixels. Deze waarden zijn precies wat als breekpunten aan de Responsieve Bibliotheek van het Beeld wordt overgegaan. Als zodanig zorgt Dynamic Media ervoor dat de netwerkbandbreedte van de client effectief wordt gebruikt. En het zorgt er ook voor dat de afbeelding wordt weergegeven in de juiste grootte, gezien de huidige lay-out van de webpagina, zonder dat visuele vervormingen de clientbrowser schalen. </p> <p>Klik URL zodat opent u de Web-pagina, resize het browser venster om verschillende lay-outbreekpunten te raken, en netwerkverkeer te controleren. </p> <p>Gevallen van geavanceerder gebruik omvatten het associëren van verschillende Voorinstellingen van het Beeld, of Beeld die bevelen, of allebei, met verschillende breekpuntwaarden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In dit volgende voorbeeld worden voorinstellingen voor afbeeldingen van verschillende afbeeldingskwaliteit en indeling voor verschillende onderbrekingspuntformaten gebruikt. Voor een klein breekpunt wordt een voorinstelling van lage kwaliteit toegepast. Deze voorinstelling dwingt Image Serving om de GIF-afbeelding die is gecomprimeerd tot slechts zes kleuren te retourneren. Een middelgroot breekpunt is het gebruiken van een Vooraf ingestelde Beeld die voor JPEG met hoge compressie wordt gevormd. Het grootste breekpunt is gekoppeld aan een voorinstelling voor afbeeldingen van hoge kwaliteit die gebruikmaakt van PNG-bestanden zonder verlies. Deze methode zorgt ervoor dat beelden van hoge kwaliteit aan dergelijke apparaten worden geleverd, gebaseerd op de veronderstelling dat de apparaten met grotere schermen grotere bandbreedte en verwerkingscapaciteit hebben. </p> <p>Klik op de URL, zodat u de webpagina opent, de grootte van het venster van de webbrowser wijzigt van groter naar kleiner en u ziet hoe de kwaliteit van de afbeelding afneemt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Naast Voorinstellingen afbeelding is het mogelijk om specifieke opdrachten voor het leveren van afbeeldingen te koppelen aan onderbrekingspunten. In het volgende voorbeeld ziet u hoe u de bannerafbeelding geleidelijk kunt uitsnijden naar het interessegebied wanneer de afbeeldingsgrootte op het scherm kleiner wordt. Hier, heeft het grootste breekpunt geen Beeld dat bevelen in dienst heeft, zodat is het bannerbeeld volledig zichtbaar. Bij een middelgroot breekpunt wordt matig uitsnijden toegepast, waardoor alleen de runner met tekst 'Running' zichtbaar wordt. Bij een klein breekpunt wordt meer bijsnijden toegepast, zodat alleen het product wordt weergegeven. </p> <p>Klik op de URL, zodat u de webpagina opent en het browservenster vergroot of verkleint. U ziet hoe de afbeelding geleidelijk wordt uitgesneden als u van groter naar kleiner formaat gaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>U kunt ook opdrachten voor Beeldservers gebruiken met Beeldservers om bepaalde sjabloonparameters te beheren op basis van de afbeeldingsgrootte. In dit volgende voorbeeld wordt een afbeeldingsserversjabloon gebruikt waar de tekengrootte van de tekstbedekking wordt geparametriseerd met de parameter <span class="codeph"> $fontsize </span>. Responsieve afbeelding is geconfigureerd om een grotere tekengrootte te gebruiken voor kleinere afbeeldingsgrootten, zodat de tekst altijd leesbaar blijft: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Systeemvereisten {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Serverhardware en -software**

* Dynamic Media Image Serving 6.0.1 of hoger.

**Minimumeisen voor de clientbrowser**

* Microsoft® Windows® 7 of hoger; macOS X 10.8 of hoger.
* Firefox 23, Safari 6, Chrome 29, IE 9 of hoger.
* iOS 6 of hoger.
* Gecertificeerd op iPhone3GS of hoger en iPad2 of hoger (alleen in native browsers).
* Android™ OS 2.3 of hoger.
* Internet Explorer op mobiele apparaten wordt momenteel niet ondersteund.
