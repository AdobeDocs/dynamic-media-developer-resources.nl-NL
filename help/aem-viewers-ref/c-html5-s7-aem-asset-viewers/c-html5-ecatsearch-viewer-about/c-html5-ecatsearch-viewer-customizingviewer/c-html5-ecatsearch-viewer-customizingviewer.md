---
title: De eCatalog Search Viewer aanpassen
description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de eCatalogKijker van het Onderzoek worden gedaan door een douane CSS te creëren.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---

# De eCatalog Search Viewer aanpassen{#customizing-ecatalog-search-viewer}

Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de eCatalogKijker van het Onderzoek worden gedaan door een douane CSS te creëren.

De voorgestelde workflow is om het standaard CSS-bestand voor de juiste viewer te gebruiken, het naar een andere locatie te kopiëren, het aan te passen en de locatie van het aangepaste bestand op te geven in het `style=` gebruiken.

Standaard CSS-bestanden vindt u op de volgende locatie:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Het aangepaste CSS-bestand moet dezelfde klassedeclaraties bevatten als de standaarddeclaratie. Als een klassendeclaratie wordt weggelaten, werkt de viewer niet correct omdat deze geen ingebouwde standaardstijlen voor de gebruikersinterface-elementen bevat.

Een andere manier om aangepaste CSS-regels te bieden, is door ingesloten stijlen rechtstreeks op de webpagina of in een van de gekoppelde externe CSS-regels te gebruiken.

Houd er bij het maken van aangepaste CSS rekening mee dat de viewer `.s7ecatalogsearchviewer` -klasse aan het DOM-containerelement. Als u een extern CSS-bestand gebruikt dat wordt doorgegeven met het `style=` gebruiken `.s7ecatalogsearchviewer` klasse als bovenliggende klasse in afstammende kiezer voor uw CSS-regels. Als u ingesloten stijlen op de webpagina uitvoert, moet u deze kiezer ook als volgt kwalificeren met een id van het DOM-containerelement:

`#<containerId>.s7ecatalogsearchviewer`

## Responsieve CSS maken {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Het is mogelijk om verschillende apparaten en insluitingsgrootten in CSS als doel in te stellen om de weergave van uw inhoud te wijzigen, afhankelijk van het apparaat van de gebruiker of een bepaalde webpaginalay-out. Dit geldt onder andere voor verschillende webpaginalay-outs, de grootte van gebruikersinterface-elementen en de resolutie van illustraties.

De viewer ondersteunt twee methoden voor het maken van responsieve, ontworpen CSS: CSS-markeringen en standaard CSS-mediaquery&#39;s. U kunt deze methoden afzonderlijk of samen gebruiken.

**CSS-markeringen**

Om responsieve, ontworpen CSS te maken, ondersteunt de viewer CSS-markeringen die speciale CSS-klassen dynamisch worden toegewezen aan het containerelement op het hoogste niveau van de viewer op basis van de viewergrootte tijdens runtime en het invoertype op het huidige apparaat.

De eerste groep CSS-markeringen bevat `.s7size_large`, `.s7size_medium`, en `.s7size_small` klassen. Ze worden toegepast op basis van het runtimegebied van de viewercontainer. Dit betekent dat het viewergebied gelijk is aan of groter is dan het formaat van een algemene desktopmonitor `.s7size_large` wordt gebruikt; als het gebied zich in de buurt van een gebruikelijke tabletvorm bevindt `.s7size_medium` is toegewezen. Voor gebieden die vergelijkbaar zijn met mobiele-telefoonschermen. De markering `.s7size_small` is ingesteld. Het belangrijkste doel van deze CSS-markeringen is het maken van verschillende lay-outs voor de gebruikersinterface voor verschillende schermen en viewerformaten.

De tweede groep CSS-markeertekens bevat `.s7mouseinput` en `.s7touchinput`. De markering `.s7touchinput` wordt ingesteld als het huidige apparaat aanraakinvoermogelijkheden heeft; anders `.s7mouseinput` wordt gebruikt. Deze markeringen zijn bedoeld om invoerelementen voor de gebruikersinterface te maken met verschillende schermgrootten voor verschillende invoertypen, omdat aanraakinvoer doorgaans grotere elementen vereist. Als het apparaat zowel muisinvoer- als aanraakmogelijkheden heeft, `.s7touchinput` wordt ingesteld en de viewer een aanraakvriendelijke gebruikersinterface weergeeft.

In het volgende voorbeeld-CSS wordt de inzoomknopgrootte ingesteld op 28 x 28 pixels op systemen met muisinvoer en op 56 x 56 pixels op aanraakapparaten. Bovendien wordt de knop volledig verborgen als de viewergrootte te klein wordt:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Gebruik CSS-mediaquery&#39;s om apparaten met een andere pixeldichtheid als doel in te stellen. Het volgende mediaqueryblok bevat CSS die specifiek is voor schermen met hoge dichtheid:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Het gebruik van CSS-markeringen is de meest flexibele manier om responsieve, ontworpen CSS samen te stellen. Hiermee kunt u niet alleen de schermgrootte van het apparaat instellen, maar ook de daadwerkelijke viewergrootte. Dit is handig voor responsieve, ontworpen paginalay-outs.

Gebruik het CSS-bestand voor de standaardviewer als voorbeeld van een CSS-markeertekenaanpak.

**CSS-mediaquery&#39;s**

Apparaatdetectie kan ook worden uitgevoerd met zuivere CSS-mediaquery&#39;s. Alles wat in een bepaald mediaqueryblok is ingesloten, wordt alleen toegepast wanneer dit op een overeenkomstig apparaat wordt uitgevoerd.

Gebruik bij toepassing op mobiele viewers vier CSS-mediaquery&#39;s die in de volgende volgorde in uw CSS zijn gedefinieerd:

1. Bevat alleen regels die specifiek zijn voor alle aanraakapparaten.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

1. Bevat alleen specifieke regels voor mobiele telefoons met schermen met hoge resolutie.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Met een mediaqueryaanpak moet u CSS met apparaatdetectie als volgt ordenen:

* Ten eerste definieert de desktopspecifieke sectie alle eigenschappen die specifiek zijn voor het bureaublad of die op alle schermen van toepassing zijn.
* Ten tweede gaan de vier mediaquery&#39;s in de hierboven gedefinieerde volgorde en bieden ze CSS-regels die specifiek zijn voor het overeenkomstige apparaattype.

Het is niet nodig om de volledige viewer-CSS in elke mediaquery te dupliceren. Alleen eigenschappen die specifiek zijn voor bepaalde apparaten, worden opnieuw gedefinieerd in een mediaquery.

## CSS-sprites {#section-9d570f95eb2443aca74c1b02f6e89aff}

Veel gebruikersinterface-elementen van de viewer worden opgemaakt met behulp van bitmapillustraties en hebben meer dan één specifieke visuele status. Een goed voorbeeld is een knop met normaal ten minste drie verschillende toestanden: &quot;omhoog&quot;, &quot;boven&quot; en &quot;omlaag&quot;. Elke status vereist een eigen toegewezen bitmapillustratie.

Bij een klassieke benadering van opmaak zou de CSS een afzonderlijke verwijzing naar het afzonderlijke afbeeldingsbestand op de server hebben voor elke status van het interface-element. Hier volgt een voorbeeld-CSS voor het opmaken van een inzoomknop:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Het nadeel van deze aanpak is dat de eindgebruiker een flikkerende of vertraagde reactie van de gebruikersinterface ervaart wanneer het element voor het eerst wordt gebruikt. Deze handeling treedt op omdat de afbeeldingsillustratie voor de nieuwe elementstatus nog niet is gedownload. Deze aanpak kan ook een enigszins negatief effect hebben op de prestaties als gevolg van een toename van het aantal HTTP-aanroepen naar de server.

CSS-sprites is een andere aanpak waarbij afbeeldingsillustraties voor alle elementstatussen worden gecombineerd in één PNG-bestand dat een &#39;sprite&#39; wordt genoemd. Zulk &quot;SPRITE&quot;heeft alle visuele staten voor het bepaalde die element één na een andere wordt geplaatst. Wanneer het stileren van een gebruikersinterface element met sprites, wordt het zelfde SPRITE beeld van verwijzingen voorzien voor alle verschillende staten in CSS. Ook de `background-position` eigenschap wordt voor elke status gebruikt om aan te geven welk deel van de &quot;sprite&quot;-afbeelding wordt gebruikt. U kunt een sprite-afbeelding op elke gewenste manier structureren. De kijkers hebben het gewoonlijk verticaal gestapeld. Hieronder ziet u een op sprite gebaseerd voorbeeld waarin u dezelfde inzoomknop van bovenaf opmaakt:

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Algemene opmaakopmerkingen en advies {#section-95855dccbbc444e79970f1aaa3260b7b}

* Wanneer u de gebruikersinterface van de viewer aanpast met CSS, kunt u de optie `!IMPORTANT` regel wordt niet ondersteund voor het opmaken van viewerelementen. Met name: `!IMPORTANT` Deze regel mag niet worden gebruikt om standaardstijlen of runtimestijlen van de viewer of Viewer SDK te negeren. De reden hiervoor is dat het het gedrag van juiste componenten kan beïnvloeden. Gebruik in plaats daarvan CSS-kiezers met de juiste specificiteit om CSS-eigenschappen in te stellen die in deze naslaggids worden beschreven.
* Alle paden naar externe elementen in CSS worden omgezet op de CSS-locatie, niet op de locatie van de HTML-pagina van de viewer. Houd rekening met deze regel wanneer u de standaard-CSS naar een andere locatie kopieert. Kopieer de standaardelementen of werk paden bij in de aangepaste CSS.
* De voorkeursindeling voor bitmapillustraties is PNG.
* Bitmapillustraties worden aan de hand van de `background-image` eigenschap.
* De `width` en `height` eigenschappen van een interface-element definiëren de logische grootte ervan. De grootte van de bitmap die wordt doorgegeven aan `background-image` heeft geen invloed op de logische grootte.
* Als u de hoge pixeldichtheid van schermen met hoge resolutie, zoals Retina, wilt gebruiken, geeft u bitmapillustraties twee keer zo groot op als de logische grootte van de gebruikersinterface-elementen. Pas vervolgens de `-webkit-background-size:contain` eigenschap om de achtergrond naar beneden te schalen naar de logische grootte van het gebruikersinterface-element.
* Als u een knop uit de gebruikersinterface wilt verwijderen, voegt u `display:none` naar de CSS-klasse.
* U kunt verschillende indelingen gebruiken voor kleurwaarden die CSS ondersteunt. Gebruik de indeling als u transparantie nodig hebt `rgba(R,G,B,A)`. Anders kunt u de indeling gebruiken `#RRGGBB`.

## Algemene gebruikersinterface-elementen {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Hier volgt de documentatie van de gebruikersinterface-elementen die van toepassing is op de eCatalog Search Viewer:

* [Knop Favoriet toevoegen](r-html5-ecatsearch-customize-addfavorite.md)
* [Knop Sluiten](r-html5-ecatsearch-customize-closebutton.md)
* [Downloaden](r-html5-ecatsearch-customize-download.md)
* [E-mailshare](r-html5-ecatsearch-customize-emailshare.md)
* [Delen insluiten](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook share](r-html5-ecatsearch-customize-facebookshare.md)
* [Favorieten, effect](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Favorieten](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Weergave Favorieten](r-html5-ecatsearch-customize-favoritesview.md)
* [Knop Eerste pagina](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Focus markeren](r-html5-ecatsearch-customize-focushighlight.md)
* [schermvullende knop](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Pictogram, effect](r-html5-ecatsearch-customize-iconeffect.md)
* [Pop-up deelvenster Info](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Afbeeldingskaart, effect](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Grote knop Volgende pagina](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Knop Grote vorige pagina](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Knop Laatste pagina](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Delen van koppeling](r-html5-ecatsearch-customize-linkshare.md)
* [Hoofdbesturingsbalk](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Hoofdgebied van viewer](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Knop Volgende pagina](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Pagina-indicator](r-html5-ecatsearch-customize-pageindicator.md)
* [Paginaweergave](r-html5-ecatsearch-customize-pageview.md)
* [Knop Vorige pagina](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Afdrukken](r-html5-ecatsearch-customize-print.md)
* [Knop Favoriet verwijderen](r-html5-ecatsearch-customize-removefavorite.md)
* [Knop Zoeken](r-html5-ecatsearch-customize-searchbutton.md)
* [Zoeken, effect](r-html5-ecatsearch-customize-searcheffect.md)
* [Deelvenster Zoekresultaten](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Secundaire besturingsbalk](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Sociaal aandeel](r-html5-ecatsearch-customize-socialshare.md)
* [Inhoudsopgave](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniaturen](r-html5-ecatsearch-customize-thumbnails.md)
* [Knop Miniaturen](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Knopinfo](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter delen](r-html5-ecatsearch-customize-twittershare.md)
* [De knop Alle favorieten weergeven](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Knop Inzoomen](r-html5-ecatsearch-customize-zoominbutton.md)
* [Knop Uitzoomen](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Knop Zoomen opnieuw instellen](r-html5-ecatsearch-customize-zoomresetbutton.md)
