---
description: Responsieve afbeeldingsbibliotheek is een JavaScript-module waarmee de kwaliteit van afbeeldingen die vanuit Scene7 worden aangeboden en die worden ingesloten in responsieve webpagina's, dynamisch wordt aangepast. Bovendien biedt de klasse een verbeterde beeldkwaliteit op apparaten met schermen met hoge dichtheid. De bibliotheek kan ook responsief resultaten renderen van Slim uitsnijden en Slim staal.
seo-description: Responsieve afbeeldingsbibliotheek is een JavaScript-module waarmee de kwaliteit van afbeeldingen die vanuit Scene7 worden aangeboden en die worden ingesloten in responsieve webpagina's, dynamisch wordt aangepast. Bovendien biedt de klasse een verbeterde beeldkwaliteit op apparaten met schermen met hoge dichtheid. De bibliotheek kan ook responsief resultaten renderen van Slim uitsnijden en Slim staal.
seo-title: De bibliotheek met responsieve afbeeldingen
solution: Experience Manager
title: De bibliotheek met responsieve afbeeldingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# Info over bibliotheek met responsieve afbeeldingen{#about-responsive-image-library}

Responsieve afbeeldingsbibliotheek is een JavaScript-module waarmee de kwaliteit van afbeeldingen die vanuit Scene7 worden aangeboden en die worden ingesloten in responsieve webpagina&#39;s, dynamisch wordt aangepast. Bovendien biedt de klasse een verbeterde beeldkwaliteit op apparaten met schermen met hoge dichtheid. De bibliotheek kan ook responsief resultaten renderen van Slim uitsnijden en Slim staal.

## URL&#39;s demo {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Het eenvoudigste gebruik van de bibliotheek met responsieve afbeeldingen is het definiëren van een lijst met onderbrekingspuntwaarden voor de afbeeldingsbreedte. Deze lijst zorgt ervoor dat de juiste vertoning wordt geladen en weergegeven wanneer de grootte van een afbeelding wordt gewijzigd omdat de webpaginalay-out is gewijzigd doordat de gebruiker het browservenster vergroot of verkleint of de richting van het apparaat wijzigt. De bibliotheek controleert voortdurend de afbeeldingsgrootte op het scherm en elke keer dat een nieuwe breedte voor een onderbrekingspunt wordt bereikt, wordt een nieuwe afbeeldingsuitvoering opgehaald uit Scene7.

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
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>In het volgende voorbeeld ziet u hoe de responsieve afbeelding zich in een container bevindt die 50% van de breedte van de webpagina in beslag neemt. Telkens wanneer de grootte van het browservenster wordt gewijzigd, verandert de breedte van de container. Wanneer de afbeeldingsbreedte een van de geconfigureerde onderbrekingspunten bereikt, die voor illustratieve doeleinden zijn ingesteld op 200, 400, 600 en 800 pixels, wordt een nieuwe uitvoering gedownload en weergegeven. Het doel is het laden van onnodige grote afbeeldingen te voorkomen en netwerkbandbreedte te besparen. </p> <p>Klik op de URL om de webpagina te openen, het browservenster te vergroten of te verkleinen en het netwerkverkeer te controleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>In het volgende Bootstrap-voorbeeld wordt hetzelfde gebruiksgeval in een webpagina getoond. Volgens Bootstrap CSS kan de lay-outcel waaraan de responsieve afbeelding wordt toegevoegd, een van de volgende breedten hebben: 360, 720 en 940 pixels. Dit zijn de exacte waarden die als breekpunten aan de Responsieve Bibliotheek van het Beeld worden overgegaan. Als zodanig zorgt Scene7 ervoor dat de netwerkbandbreedte van de client effectief wordt gebruikt. En het zorgt er ook voor dat de afbeelding wordt weergegeven in de juiste grootte, gezien de huidige lay-out van de webpagina, zonder dat visuele vervormingen de clientbrowser schalen. </p> <p>Klik op de URL om de webpagina te openen, wijzig de grootte van het browservenster om verschillende onderbrekingspunten in de layout te bereiken en controleer het netwerkverkeer. </p> <p>Gevallen van geavanceerder gebruik omvatten het associëren van verschillende Voorinstellingen van het Beeld, of Beeld die bevelen, of allebei, met verschillende breekpuntwaarden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In dit volgende voorbeeld worden voorinstellingen voor afbeeldingen van verschillende afbeeldingskwaliteit en indeling voor verschillende onderbrekingspuntformaten gebruikt. Voor een klein breekpunt wordt een voorinstelling van lage kwaliteit toegepast. Deze voorinstelling dwingt Image Serving om de GIF-afbeelding die is gecomprimeerd tot slechts zes kleuren te retourneren. Een middelgroot breekpunt is het gebruiken van een Vooraf ingestelde Beeld die voor JPEG met hoge compressie wordt gevormd. Het grootste breekpunt is gekoppeld aan een voorinstelling voor afbeeldingen van hoge kwaliteit die gebruikmaakt van PNG-bestanden zonder verlies. Deze methode zorgt ervoor dat beelden van hoge kwaliteit aan dergelijke apparaten worden geleverd, gebaseerd op de veronderstelling dat de apparaten met grotere schermen grotere bandbreedte en verwerkingscapaciteit hebben. </p> <p>Klik op de URL om de webpagina te openen, wijzig de grootte van het venster van de webbrowser van groter naar kleiner en zie hoe de afbeeldingskwaliteit afneemt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Naast Voorinstellingen afbeelding is het mogelijk om specifieke opdrachten voor het leveren van afbeeldingen te koppelen aan onderbrekingspunten. In het volgende voorbeeld ziet u hoe u de bannerafbeelding geleidelijk kunt uitsnijden naar het interessegebied wanneer de afbeeldingsgrootte op het scherm kleiner wordt. Hier, heeft het grootste breekpunt geen Beeld dat bevelen in dienst heeft, zodat is het bannerbeeld volledig zichtbaar. Bij een middelgroot breekpunt wordt matig uitsnijden toegepast, waardoor alleen de runner met tekst 'Running' zichtbaar wordt. Bij een klein breekpunt wordt meer bijsnijden toegepast, zodat alleen het product wordt weergegeven. </p> <p>Klik op de URL om de webpagina te openen en het browservenster te vergroten of te verkleinen. U ziet hoe de afbeelding geleidelijk wordt uitgesneden als u van groter naar kleiner formaat gaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>U kunt ook opdrachten voor Beeldservers gebruiken met Beeldservers om bepaalde sjabloonparameters te beheren op basis van de afbeeldingsgrootte. In dit volgende voorbeeld wordt een afbeeldingsserversjabloon gebruikt waar de tekengrootte van de tekstbedekking wordt geparametriseerd met de parameter <span class="codeph"> $fontsize </span>. Responsieve afbeelding is geconfigureerd om een grotere tekengrootte te gebruiken voor kleinere afbeeldingsgrootten, zodat de tekst altijd leesbaar blijft: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Systeemvereisten {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Serverhardware en -software**

* Scene7 Image Serving 6.0.1 of hoger.

**Minimumeisen voor de clientbrowser**

* Microsoft® Windows® 7 of hoger; Mac OS X 10.8 of hoger.
* Firefox 23, Safari 6, Chrome 29, IE 9 of hoger.
* iOS 6 of hoger.
* Gecertificeerd op iPhone3GS of hoger en iPad2 of hoger (alleen in native browsers).
* Android OS 2.3 of hoger.
* Internet Explorer op mobiele apparaten wordt momenteel niet ondersteund.

