---
description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Interactive Image Viewer worden uitgevoerd door een aangepaste CSS te maken.
keywords: responsive
seo-description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Interactive Image Viewer worden uitgevoerd door een aangepaste CSS te maken.
seo-title: Interactieve afbeeldingsviewer aanpassen
solution: Experience Manager
title: Interactieve afbeeldingsviewer aanpassen
topic: Dynamic media
uuid: 19868e4e-c2c9-41e0-82a6-20884a9454a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 0%

---


# Interactieve afbeeldingsviewer aanpassen{#customizing-interactive-image-viewer}

Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Interactive Image Viewer worden uitgevoerd door een aangepaste CSS te maken.

De voorgestelde workflow is om het standaard CSS-bestand voor de juiste viewer te gebruiken, het naar een andere locatie te kopiëren, het aan te passen en de locatie van het aangepaste bestand op te geven in de opdracht `style=`.

Standaard CSS-bestanden vindt u op de volgende locatie:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

Aangepast CSS-bestand moet dezelfde klassedeclaraties bevatten als het standaardbestand. Als een klassendeclaratie wordt weggelaten, werkt de viewer niet correct omdat deze geen ingebouwde standaardstijlen voor gebruikersinterface-elementen biedt.

Een andere manier om aangepaste CSS-regels te bieden, is door ingesloten stijlen rechtstreeks op de webpagina of in een van gekoppelde externe CSS-regels te gebruiken.

Houd er bij het maken van aangepaste CSS rekening mee dat de viewer de klasse `.s7interactiveimage` toewijst aan het DOM-containerelement. Als u een extern CSS dossier gebruikt dat met `style=` bevel wordt overgegaan, gebruik `.s7interactiveimage` klasse als ouderklasse in dalende selecteur voor uw CSS regels. Als u ingesloten stijlen aan de webpagina toevoegt, kwalificeert u deze kiezer als volgt aanvullend met een id van het DOM-containerelement:

`#<containerId>.s7interactiveimage`

## Responsieve ontworpen CSS maken {#section-0bb49aca42d242d9b01879d5ba59d33b}

Het is mogelijk om verschillende apparaten en insluitingsgrootten in CSS als doel in te stellen om de weergave van uw inhoud anders te maken, afhankelijk van het apparaat van de gebruiker of een bepaalde webpaginalay-out. Dit omvat onder andere, maar is niet beperkt tot, verschillende lay-outs, de grootte van gebruikersinterface-elementen en de resolutie van illustraties.

De viewer ondersteunt twee mechanismen voor het maken van responsieve, ontworpen CSS: CSS-markeringen en standaard CSS-mediaquery&#39;s. U kunt deze onafhankelijk of samen gebruiken.

**CSS-markeringen**

Voor hulp bij het maken van responsieve, ontworpen CSS, ondersteunt de viewer CSS-markeringen. Dit zijn speciale CSS-klassen die dynamisch worden toegewezen aan het viewer-containerelement op hoofdniveau. Ze zijn gebaseerd op de grootte van de runtimeviewer en het invoertype dat op het huidige apparaat wordt gebruikt.

De eerste groep CSS-markeringen bevat `.s7size_large`, `.s7size_medium` en `.s7size_small` klassen. Ze worden toegepast op basis van het runtimegebied van de viewercontainer. Als het viewergebied bijvoorbeeld gelijk is aan of groter is dan het formaat van een algemene desktopmonitor, gebruikt u `.s7size_large`. Wijs `.s7size_medium` toe als het gebied zich dicht bij een gewoon tabletapparaat bevindt. Gebruik `.s7size_small` voor gebieden die vergelijkbaar zijn met mobiele-telefoonschermen. Het belangrijkste doel van deze CSS-markeringen is het maken van verschillende lay-outs voor de gebruikersinterface voor verschillende schermen en viewerformaten.

De tweede groep CSS-markeringen bevat `.s7mouseinput` en `.s7touchinput`. De CSS-markering `.s7touchinput` wordt ingesteld als het huidige apparaat aanraakinvoer kan gebruiken. Anders wordt `.s7mouseinput` gebruikt. Deze markeringen zijn vooral bedoeld om invoerelementen in de gebruikersinterface te maken met verschillende schermgrootten voor verschillende invoertypen, omdat aanraakinvoer doorgaans grotere elementen vereist.

In het volgende voorbeeld-CSS wordt de inzoomknopgrootte ingesteld op 28 x 28 pixels op systemen met muisinvoer en op 56 x 56 pixels op aanraakinvoerapparaten. Als de grootte van de viewer nog kleiner is, wordt deze ingesteld op 20 x 20 pixels.

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
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

Gebruik bij toepassing op mobiele viewers vier CSS-mediaquery&#39;s, die in uw CSS zijn gedefinieerd, in de onderstaande volgorde:

1. Bevat alleen regels die specifiek zijn voor alle aanraakapparaten.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Bevat alleen specifieke regels voor tablets met schermen met hoge resolutie.

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

1. Bevat alleen specifieke regels voor mobiele telefoons met schermen met hoge resolutie.

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

Veel gebruikersinterface-elementen van de viewer worden opgemaakt met behulp van bitmapillustraties en hebben meer dan één specifieke visuele status. Een goed voorbeeld is een knop die normaal ten minste drie verschillende toestanden heeft: `up`, `over` en `down`. Elke status vereist een eigen toegewezen bitmapillustratie.

Bij een klassieke benadering van opmaak zou de CSS een afzonderlijke verwijzing naar het afzonderlijke afbeeldingsbestand op de server hebben voor elke status van het interface-element. Hier volgt een voorbeeld-CSS voor het opmaken van een inzoomknop:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

Het nadeel van deze aanpak is dat de eindgebruiker een flikkerende of vertraagde reactie van de gebruikersinterface ervaart wanneer het element voor het eerst wordt gebruikt. Deze handeling treedt op omdat de afbeeldingsillustratie voor de nieuwe elementstatus nog niet is gedownload. Deze aanpak kan ook een enigszins negatief effect hebben op de prestaties als gevolg van een toename van het aantal HTTP-aanroepen naar de server.

CSS-sprites is een andere aanpak waarbij afbeeldingsillustraties voor alle elementstatussen worden gecombineerd in één PNG-bestand dat een &#39;sprite&#39; wordt genoemd. Zulk &quot;SPRITE&quot;heeft alle visuele staten voor het bepaalde die element één na een andere wordt geplaatst. Bij het opmaken van een gebruikersinterface-element met sprites wordt naar dezelfde sprite-afbeelding verwezen voor alle verschillende statussen in de CSS. Ook, wordt het `background-position` bezit gebruikt voor elke staat om te specificeren welk deel van het &quot;SPRITE&quot;beeld wordt gebruikt. U kunt een sprite-afbeelding op elke gewenste manier structureren. De kijkers hebben het gewoonlijk verticaal gestapeld.

Hieronder ziet u een op sprites gebaseerd voorbeeld waarin u dezelfde inzoomknop eerder opmaakt:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Algemene opmaaknotities en advies {#section-95855dccbbc444e79970f1aaa3260b7b}

* Wanneer u de gebruikersinterface van de viewer aanpast met CSS, wordt het gebruik van de regel `!IMPORTANT` niet ondersteund voor het opmaken van viewerelementen. Met name `!IMPORTANT`-regel mag niet worden gebruikt om standaardstijlen of runtimestijlen van de viewer of Viewer SDK te negeren. De reden hiervoor is dat het gedrag van juiste componenten kan beïnvloeden. Gebruik in plaats daarvan CSS-kiezers met de juiste specificiteit om CSS-eigenschappen in te stellen die in deze naslaggids voor viewers worden beschreven.
* Alle paden naar externe elementen in CSS worden omgezet op de CSS-locatie, niet op de locatie van de HTML-pagina van de viewer. Houd rekening met deze regel wanneer u de standaard-CSS naar een andere locatie kopieert. Kopieer de standaardelementen of werk alle paden in de aangepaste CSS bij.
* De voorkeursindeling voor bitmapillustraties is PNG.
* Bitmapillustraties worden met de eigenschap `background-image` toegewezen aan elementen van de gebruikersinterface.
* De `width` en `height` eigenschappen van een gebruikersinterface-element bepalen zijn logische grootte. De grootte van de bitmap die wordt doorgegeven aan `background-image` heeft geen invloed op de logische grootte ervan.
* Als u de hoge pixeldichtheid van schermen met hoge resolutie, zoals Retina, wilt gebruiken, geeft u bitmapillustraties twee keer zo groot op als de logische grootte van de gebruikersinterface-elementen. Pas vervolgens de eigenschap `-webkit-background-size:contain` toe om de achtergrond omlaag te schalen naar de logische grootte van het interface-element.
* Als u een knop uit de gebruikersinterface wilt verwijderen, voegt u `display:none` toe aan de CSS-klasse.
* U kunt verschillende indelingen gebruiken voor kleurwaarden die door CSS worden ondersteund. Als u transparantie nodig hebt, gebruikt u de notatie `rgba(R,G,B,A)`. Anders kunt u de notatie `#RRGGBB` gebruiken.

## Algemene elementen van de gebruikersinterface {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Hier volgt de documentatie van de gebruikersinterface-elementen die van toepassing is op de Video Image Viewer:
