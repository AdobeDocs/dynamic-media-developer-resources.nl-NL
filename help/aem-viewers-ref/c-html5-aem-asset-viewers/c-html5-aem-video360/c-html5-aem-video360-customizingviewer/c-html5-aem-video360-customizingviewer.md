---
description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Video360 Viewer worden uitgevoerd door een aangepaste CSS te maken.
keywords: responsive
seo-description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Video360 Viewer worden uitgevoerd door een aangepaste CSS te maken.
seo-title: Video360 Viewer aanpassen
solution: Experience Manager
title: Video360 Viewer aanpassen
topic: Dynamic media
uuid: 1f021a11-856e-4bbc-a2ee-454ab0a60adb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360 Viewer aanpassen{#customizing-video-viewer}

Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Video360 Viewer worden uitgevoerd door een aangepaste CSS te maken.

De voorgestelde workflow is om het standaard CSS-bestand voor de juiste viewer te gebruiken, het naar een andere locatie te kopiëren, het aan te passen en de locatie van het aangepaste bestand in de `style=` opdracht op te geven.

Standaard CSS-bestanden vindt u op de volgende locatie:

`<s7_viewers_root>/html5/Video360Viewer_dark.css`

Het aangepaste CSS-bestand moet dezelfde klassedeclaraties bevatten als de standaarddeclaratie. Als een klassendeclaratie wordt weggelaten, werkt de viewer niet correct omdat deze geen ingebouwde standaardstijlen voor gebruikersinterface-elementen biedt.

Een andere manier om aangepaste CSS-regels te bieden, is door ingesloten stijlen rechtstreeks op de webpagina of in een van gekoppelde externe CSS-regels te gebruiken.

Wanneer u aangepaste CSS maakt, moet u er rekening mee houden dat de viewer `.s7video360viewer` klasse toewijst aan het container DOM-element. Als u extern CSS-bestand gebruikt dat met `style=` de opdracht is doorgegeven, gebruikt u `.s7video360viewer` klasse als bovenliggende klasse in de onderliggende kiezer voor uw CSS-regels. Als u ingesloten stijlen op de webpagina uitvoert, kwalificeert u deze kiezer als volgt aanvullend met een id van het DOM-containerelement:

`#<containerId>.s7video360viewer`

## Responsieve CSS maken {#section-0bb49aca42d242d9b01879d5ba59d33b}

Het is mogelijk om verschillende apparaten en insluitingsgrootten in CSS als doel in te stellen om uw inhoudsweergave te wijzigen, afhankelijk van het apparaat van de gebruiker of een bepaalde webpagina-indeling. Dit omvat onder andere, maar is niet beperkt tot, verschillende lay-outs, de grootte van gebruikersinterface-elementen en de resolutie van illustraties.

De viewer ondersteunt twee mechanismen voor het maken van responsieve, ontworpen CSS: CSS-markeringen en standaard CSS-mediaquery&#39;s. U kunt deze onafhankelijk of samen gebruiken.

**CSS-markeringen**

Voor hulp bij het maken van responsieve, ontworpen CSS, ondersteunt de viewer CSS-markeringen. Dit zijn speciale CSS-klassen die dynamisch worden toegewezen aan het viewercontainerelement op het hoogste niveau op basis van de viewergrootte tijdens runtime en het invoertype dat op het huidige apparaat wordt gebruikt.

De eerste groep CSS-markeringen bevat `.s7size_large`, `.s7size_medium`en `.s7size_small` klassen. Ze worden toegepast op basis van het runtimegebied van de viewercontainer. Als het viewergebied gelijk is aan of groter is dan het formaat van een algemene desktopmonitor, `.s7size_large` wordt dit gebruikt. Als het gebied dicht bij een gebruikelijke tabletapparaat ligt, `.s7size_medium` wordt het toegewezen. Voor gebieden die vergelijkbaar zijn met mobiele-telefoonschermen `.s7size_small` wordt deze instelling ingesteld. Het belangrijkste doel van deze CSS-markeringen is het maken van verschillende lay-outs voor de gebruikersinterface voor verschillende schermen en viewerformaten.

De tweede groep CSS-markeertekens bevat `.s7mouseinput` en `.s7touchinput`. `.s7touchinput` wordt ingesteld als het huidige apparaat aanraakinvoermogelijkheden heeft; anders, `.s7mouseinput` wordt gebruikt. Deze markeringen zijn vooral bedoeld om invoerelementen in de gebruikersinterface te maken met verschillende schermgrootten voor verschillende invoertypen, omdat aanraakinvoer doorgaans grotere elementen vereist. Let op: als het apparaat zowel muisinvoer als aanraakmogelijkheden heeft, `.s7touchinput` wordt dit ingesteld en geeft de viewer een aanraakvriendelijke gebruikersinterface weer.

In het volgende voorbeeld-CSS wordt de grootte van de afspeel-/pauzeknop ingesteld op 28x28 pixels op systemen met muisinvoer en 56x56 pixels op aanraakapparaten. Bovendien wordt de knop volledig verborgen als de viewergrootte aanzienlijk wordt verkleind:

```
.s7video360viewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7video360viewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7video360viewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Als u apparaten met verschillende pixeldichtheid wilt aanwijzen, moet u CSS-mediaquery&#39;s gebruiken. Het volgende mediaqueryblok bevat CSS die specifiek is voor schermen met hoge dichtheid:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Het gebruik van CSS-markeringen is de meest flexibele manier om responsieve, ontworpen CSS te maken, omdat u hiermee niet alleen de schermgrootte van het apparaat maar ook de daadwerkelijke viewergrootte kunt instellen. Dit is handig voor responsieve ontwerplay-outs.

U kunt het CSS-bestand voor de standaardviewer gebruiken als voorbeeld van een CSS-markeertekenaanpak.

**CSS-mediaquery&#39;s**

U kunt apparaatdetectie ook uitvoeren door alleen CSS-mediaquery&#39;s te gebruiken. Alles wat in een bepaald mediaqueryblok is ingesloten, wordt alleen toegepast wanneer dit op een overeenkomstig apparaat wordt uitgevoerd.

Wanneer deze worden toegepast op mobiele HTML5-viewers, gebruiken deze vier CSS-mediaquery&#39;s, die in uw CSS zijn gedefinieerd, in de onderstaande volgorde:

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

## CSS-sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Veel gebruikersinterface-elementen van de viewer worden opgemaakt met behulp van bitmapillustraties en hebben meer dan één specifieke visuele status. Een goed voorbeeld is een knop die normaal ten minste drie verschillende toestanden heeft: &quot;up&quot;, &quot;over&quot; en &quot;down&quot;. Elke status vereist een eigen toegewezen bitmapillustratie.

Bij een klassieke benadering van opmaak zou de CSS een afzonderlijke verwijzing naar het afzonderlijke afbeeldingsbestand op de server hebben voor elke status van het interface-element. Hieronder ziet u een voorbeeld-CSS voor het opmaken van een knop in een volledig scherm:

```
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

Het nadeel van deze aanpak is dat de eindgebruiker een flikkerende of vertraagde reactie van de gebruikersinterface ervaart wanneer het element voor het eerst wordt gebruikt. Deze handeling treedt op omdat de afbeeldingsillustratie voor de nieuwe elementstatus nog niet is gedownload. Deze aanpak kan ook een enigszins negatief effect hebben op de prestaties als gevolg van een toename van het aantal HTTP-aanroepen naar de server.

CSS-sprites is een andere aanpak waarbij afbeeldingsillustraties voor alle elementstatussen worden gecombineerd in één PNG-bestand dat een &#39;sprite&#39; wordt genoemd. Zulk &quot;SPRITE&quot;heeft alle visuele staten voor het bepaalde die element één na een andere wordt geplaatst. Bij het opmaken van een gebruikersinterface-element met sprites wordt naar dezelfde sprite-afbeelding verwezen voor alle verschillende statussen in de CSS. Ook, wordt het `background-position` bezit gebruikt voor elke staat om te specificeren welk deel van het &quot;SPRITE&quot;beeld wordt gebruikt. U kunt een sprite-afbeelding op elke gewenste manier structureren. De kijkers hebben het gewoonlijk verticaal gestapeld. Hieronder ziet u een op sprite gebaseerd voorbeeld waarin u dezelfde knop voor volledig scherm vroeger opmaakt:

```
.s7video360viewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Algemene opmaakopmerkingen en advies {#section-95855dccbbc444e79970f1aaa3260b7b}

* Alle paden naar externe elementen in CSS worden omgezet op de CSS-locatie, niet op de locatie van de HTML-pagina van de viewer. Houd rekening met deze regel wanneer u de standaard-CSS naar een andere locatie kopieert. Kopieer de standaardelementen of werk paden bij in de aangepaste CSS.
* De voorkeursindeling voor bitmapillustraties is PNG.
* Bitmapillustraties worden aan de elementen van de gebruikersinterface toegewezen met behulp van de `background-image` eigenschap.
* De `width` en `height` eigenschappen van een gebruikersinterface-element definiëren de logische grootte ervan. De grootte van de doorgegeven bitmap heeft `background-image` geen invloed op de logische grootte.

* Als u de hoge pixeldichtheid van schermen met hoge resolutie, zoals Retina, wilt gebruiken, geeft u bitmapillustraties twee keer zo groot op als de logische grootte van de gebruikersinterface-elementen. Pas vervolgens de `-webkit-background-size:contain` eigenschap toe om de achtergrond omlaag te schalen naar de logische grootte van het gebruikersinterface-element.
* Als u een knop uit de gebruikersinterface wilt verwijderen, voegt u deze toe `display:none` aan de CSS-klasse.
* U kunt verschillende indelingen gebruiken voor kleurwaarden die door CSS worden ondersteund. Gebruik de indeling als u transparantie nodig hebt `rgba(R,G,B,A)`. Anders kunt u de indeling gebruiken `#RRGGBB`.

* Wanneer u de gebruikersinterface van de viewer aanpast met CSS, wordt het gebruik van de `!IMPORTANT` regel niet ondersteund voor het opmaken van viewerelementen. De regel `!IMPORTANT` mag met name niet worden gebruikt om standaardstijlen of runtimestijlen die door de viewer of Viewer SDK worden geboden, te negeren. De reden hiervoor is dat het het gedrag van juiste componenten kan beïnvloeden. Gebruik in plaats daarvan CSS-kiezers met de juiste specificiteit om CSS-eigenschappen in te stellen die in deze naslaggids worden beschreven.

## Algemene gebruikersinterface-elementen {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Hieronder vindt u de referentiedocumentatie voor gebruikersinterface-elementen die van toepassing is op Video360 Viewer:
