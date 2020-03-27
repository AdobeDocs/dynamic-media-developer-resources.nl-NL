---
description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Spin Viewer worden uitgevoerd door een aangepaste CSS te maken.
keywords: responsive
seo-description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Spin Viewer worden uitgevoerd door een aangepaste CSS te maken.
seo-title: Spin Viewer aanpassen
solution: Experience Manager
title: Spin Viewer aanpassen
topic: Dynamic media
uuid: d951501c-d6da-454c-be2f-0887ffcac77c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Spin Viewer aanpassen{#customizing-spin-viewer}

Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Spin Viewer worden uitgevoerd door een aangepaste CSS te maken.

De voorgestelde workflow is om het standaard CSS-bestand voor de juiste viewer te gebruiken, het naar een andere locatie te kopiëren, het aan te passen en de locatie van het aangepaste bestand in de `style=` opdracht op te geven.

Standaard CSS-bestanden vindt u op de volgende locatie:

`<s7_viewers_root>/html5/SpinViewer_light.css`

De viewer wordt geleverd met CSS-bestanden die niet in de box staan, voor &#39;lichte&#39; en &#39;donkere&#39; kleurenschema&#39;s. De versie &quot;light&quot; wordt standaard gebruikt, maar u kunt overschakelen naar de versie &quot;donker&quot; met de volgende standaard-CSS:

`<s7_viewers_root>/html5/SpinViewer_dark.css`

Aangepast CSS-bestand moet dezelfde klassedeclaraties bevatten als het standaardbestand. Als een klassendeclaratie wordt weggelaten, werkt de viewer niet correct omdat deze geen ingebouwde standaardstijlen voor gebruikersinterface-elementen biedt.

Een andere manier om aangepaste CSS-regels te bieden, is door ingesloten stijlen rechtstreeks op de webpagina of in een van gekoppelde externe CSS-regels te gebruiken.

Houd er bij het maken van aangepaste CSS rekening mee dat de viewer `.s7spinviewer` klasse toewijst aan het container DOM-element. Als u extern CSS-bestand gebruikt dat met `style=` de opdracht is doorgegeven, gebruikt u `.s7spinviewer` klasse als bovenliggende klasse in de onderliggende kiezer voor uw CSS-regels. Als u ingesloten stijlen op de webpagina uitvoert, kwalificeert u deze kiezer als volgt aanvullend met een id van het DOM-containerelement:

`#<containerId>.s7spinviewer`

## Responsieve CSS maken {#section-0bb49aca42d242d9b01879d5ba59d33b}

Het is mogelijk om verschillende apparaten en insluitingsgrootten in CSS als doel in te stellen om de weergave van uw inhoud te wijzigen, afhankelijk van het apparaat van de gebruiker of een bepaalde webpaginalay-out. Dit geldt onder andere voor verschillende webpaginalay-outs, de grootte van gebruikersinterface-elementen en de resolutie van illustraties.

De viewer ondersteunt twee methoden voor het maken van responsieve, ontworpen CSS: CSS-markeringen en standaard CSS-mediaquery&#39;s. U kunt deze methoden afzonderlijk of samen gebruiken.

**CSS-markeringen**

Voor hulp bij het maken van responsieve, ontworpen CSS, ondersteunt de viewer CSS-markeringen die speciale CSS-klassen dynamisch worden toegewezen aan het containerelement op het hoogste niveau, gebaseerd op de viewergrootte tijdens runtime en het invoertype dat op het huidige apparaat wordt gebruikt.

De eerste groep CSS-markeringen bevat `.s7size_large`, `.s7size_medium`en `.s7size_small` klassen. Ze worden toegepast op basis van het runtimegebied van de viewercontainer. Dat wil zeggen dat het viewergebied gelijk is aan of groter is dan het formaat van een algemene desktopmonitor `.s7size_large` wordt gebruikt; als de grootte van het gebied dicht bij die van een gebruikelijke tabletapparaat `.s7size_medium` ligt. Voor gebieden die vergelijkbaar zijn met mobiele-telefoonschermen `.s7size_small` wordt ingesteld. Het belangrijkste doel van deze CSS-markeringen is het maken van verschillende lay-outs voor de gebruikersinterface voor verschillende schermen en viewerformaten.

De tweede groep CSS-markeringen bevat `.s7mouseinput` en `.s7touchinput`. `.s7touchinput` wordt ingesteld als het huidige apparaat aanraakinvoermogelijkheden heeft; anders, `.s7mouseinput` wordt gebruikt. Deze markeringen zijn bedoeld om invoerelementen voor de gebruikersinterface te maken met verschillende schermgrootten voor verschillende invoertypen, omdat aanraakinvoer doorgaans grotere elementen vereist. Als het apparaat zowel muisinvoer- als aanraakmogelijkheden heeft, `.s7touchinput` wordt dit ingesteld en wordt een aanraakvriendelijke gebruikersinterface weergegeven.

In het volgende voorbeeld-CSS wordt de inzoomknopgrootte ingesteld op 28 x 28 pixels op systemen met muisinvoer en op 56 x 56 pixels op aanraakapparaten. Bovendien wordt de knop volledig verborgen als de viewergrootte erg klein wordt:

```
.s7spinviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7spinviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7spinviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Gebruik CSS-mediaquery&#39;s om apparaten met een andere pixeldichtheid als doel in te stellen. Het volgende mediaqueryblok bevat CSS die specifiek is voor schermen met hoge dichtheid:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Het gebruik van CSS-markeertekens is de meest flexibele manier om responsieve, ontworpen CSS te maken, aangezien u hiermee niet alleen de schermgrootte van het apparaat maar ook de werkelijke viewergrootte als doel kunt instellen. Dit kan handig zijn voor responsieve ontwerppaginalay-outs.

Gebruik het CSS-bestand voor de standaardviewer als voorbeeld van een CSS-markeertekenaanpak.

**CSS-mediaquery&#39;s**

Apparaatdetectie kan ook worden uitgevoerd met zuivere CSS-mediaquery&#39;s. Alles wat in een bepaald mediaqueryblok is ingesloten, wordt alleen toegepast wanneer dit op een overeenkomstig apparaat wordt uitgevoerd.

Gebruik bij toepassing op mobiele viewers vier CSS-mediaquery&#39;s die in de volgende volgorde in uw CSS zijn gedefinieerd:

1. Bevat alleen regels die specifiek zijn voor alle aanraakapparaten.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Bevat alleen regels die specifiek zijn voor tablets met schermen met hoge resolutie.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Bevat alleen specifieke regels voor alle mobiele telefoons.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Bevat alleen regels die specifiek zijn voor mobiele telefoons met schermen met hoge resolutie.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Als u een mediaqueryaanpak gebruikt, moet u CSS met apparaatdetectie als volgt ordenen:

* Ten eerste definieert de desktopspecifieke sectie alle eigenschappen die specifiek zijn voor het bureaublad of die op alle schermen van toepassing zijn.
* Ten tweede gaan de vier mediaquery&#39;s in de hierboven gedefinieerde volgorde en bieden ze CSS-regels die specifiek zijn voor het overeenkomstige apparaattype.

Het is niet nodig om de volledige viewer-CSS in elke mediaquery te dupliceren. Alleen eigenschappen die specifiek zijn voor bepaalde apparaten, worden opnieuw gedefinieerd in een mediaquery.

## CSS-sprites {#section-b671c70acf284cb0aea678c2d2e4babc}

Veel gebruikersinterface-elementen van de viewer worden opgemaakt met behulp van bitmapillustraties en hebben meer dan één specifieke visuele status. Een goed voorbeeld is een knop die normaal ten minste drie verschillende toestanden heeft: &quot;up&quot;, &quot;over&quot; en &quot;down&quot;. Elke status vereist een eigen toegewezen bitmapillustratie.

Bij een klassieke benadering van opmaak zou de CSS een afzonderlijke verwijzing naar het afzonderlijke afbeeldingsbestand op de server hebben voor elke status van het interface-element. Hier volgt een voorbeeld van een CSS voor het opmaken van de inzoomknop:

```
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Het nadeel van deze aanpak is dat de eindgebruiker een flikkerende of vertraagde reactie van de gebruikersinterface ervaart wanneer het element voor het eerst wordt gebruikt. Deze handeling treedt op omdat de afbeeldingsillustratie voor de nieuwe elementstatus nog niet is gedownload. Deze aanpak kan ook een enigszins negatief effect hebben op de prestaties als gevolg van een toename van het aantal HTTP-aanroepen naar de server.

CSS-sprites is een andere aanpak waarbij afbeeldingsillustraties voor alle elementstatussen worden gecombineerd in één PNG-bestand dat een &#39;sprite&#39; wordt genoemd. Zulk &quot;SPRITE&quot;heeft alle visuele staten voor het bepaalde die element één na een andere wordt geplaatst. Bij het opmaken van een gebruikersinterface-element met sprites wordt naar dezelfde sprite-afbeelding verwezen voor alle verschillende statussen in de CSS. Ook, wordt het `background-position` bezit gebruikt voor elke staat om te specificeren welk deel van het &quot;SPRITE&quot;beeld wordt gebruikt. U kunt een sprite-afbeelding op elke gewenste manier structureren. De kijkers hebben het gewoonlijk verticaal gestapeld. Hieronder ziet u een op sprite gebaseerd voorbeeld waarin u dezelfde inzoomknop van bovenaf opmaakt:

```
.s7spinviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Algemene opmaakopmerkingen en advies {#section-95855dccbbc444e79970f1aaa3260b7b}

* Wanneer u de gebruikersinterface van de viewer aanpast met CSS, wordt het gebruik van de `!IMPORTANT` regel niet ondersteund voor het opmaken van viewerelementen. De regel `!IMPORTANT` mag met name niet worden gebruikt om standaardstijlen of runtimestijlen die door de viewer of Viewer SDK worden geboden, te negeren. De reden hiervoor is dat het het gedrag van juiste componenten kan beïnvloeden. Gebruik in plaats daarvan CSS-kiezers met de juiste specificiteit om CSS-eigenschappen in te stellen die in deze naslaggids worden beschreven.
* Alle paden naar externe elementen in CSS worden omgezet op de CSS-locatie, niet op de locatie van de HTML-pagina van de viewer. Houd rekening met deze regel wanneer u de standaard-CSS naar een andere locatie kopieert. Kopieer de standaardelementen of werk paden bij in de aangepaste CSS.
* De voorkeursindeling voor bitmapillustraties is PNG.
* Bitmapillustraties worden aan de elementen van de gebruikersinterface toegewezen met behulp van de `background-image` eigenschap.
* De `width` en `height` eigenschappen van een gebruikersinterface-element definiëren de logische grootte ervan. De grootte van de doorgegeven bitmap heeft `background-image` geen invloed op de logische grootte.
* Als u de hoge pixeldichtheid van schermen met hoge resolutie, zoals Retina, wilt gebruiken, geeft u bitmapillustraties twee keer zo groot op als de logische grootte van de gebruikersinterface-elementen. Pas vervolgens de `-webkit-background-size:contain` eigenschap toe om de achtergrond omlaag te schalen naar de logische grootte van het gebruikersinterface-element.
* Als u een knop uit de gebruikersinterface wilt verwijderen, voegt u deze toe `display:none` aan de CSS-klasse.
* U kunt verschillende indelingen gebruiken voor kleurwaarden die door CSS worden ondersteund. Gebruik de indeling als u transparantie nodig hebt `rgba(R,G,B,A)`. Anders kunt u de indeling gebruiken `#RRGGBB`.

## Algemene gebruikersinterface-elementen {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Hieronder vindt u de referentiedocumentatie voor gebruikersinterface-elementen die van toepassing is op de gemengde Media Viewer:
