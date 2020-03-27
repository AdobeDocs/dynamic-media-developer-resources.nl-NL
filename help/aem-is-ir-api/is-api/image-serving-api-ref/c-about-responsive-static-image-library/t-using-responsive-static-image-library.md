---
description: Voer de volgende stappen uit om een bibliotheek met responsieve afbeeldingen aan een webpagina toe te voegen en bestaande afbeeldingen met de bibliotheek te beheren.
seo-description: Voer de volgende stappen uit om een bibliotheek met responsieve afbeeldingen aan een webpagina toe te voegen en bestaande afbeeldingen met de bibliotheek te beheren.
seo-title: De bibliotheek met responsieve afbeeldingen gebruiken
solution: Experience Manager
title: De bibliotheek met responsieve afbeeldingen gebruiken
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# De bibliotheek met responsieve afbeeldingen gebruiken{#using-responsive-image-library}

Voer de volgende stappen uit om een bibliotheek met responsieve afbeeldingen aan een webpagina toe te voegen en bestaande afbeeldingen met de bibliotheek te beheren.

**De bibliotheek met responsieve afbeeldingen gebruiken**

1. In SPS, [creeer een Vooraf ingesteld](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) Beeld voor het geval u de Responsieve bibliotheek van het Beeld met vooraf instelt van plan bent te gebruiken.

   Als u voorinstellingen voor afbeeldingen definieert die worden gebruikt met de bibliotheek met responsieve afbeeldingen, gebruikt u geen instellingen die de afbeeldingsgrootte beïnvloeden, zoals `wid=`, `hei=`of `scl=`. Geef geen velden voor de grootte op in de voorinstelling Afbeelding. Laat ze in plaats daarvan leeg.
1. Voeg het JavaScript-bibliotheekbestand toe aan uw webpagina.

   Voordat u de bibliotheek-API kunt gebruiken, moet u controleren of u deze invoegt `responsive_image.js`. Dit JavaScript-bestand bevindt zich in de `libs/` submap van uw standaard IS-Viewers-implementatie:

   `<s7viewers_root>/libs/responsive_image.js`
1. Bestaande afbeeldingen instellen.

   De bibliotheek leest bepaalde configuratiekenmerken van een afbeeldingsinstantie waarmee het werkt. Definieer kenmerken voordat de API-functie voor een dergelijke afbeelding wordt aangeroepen. `s7responsiveImage`

   U kunt ook de bestaande afbeeldings-URL in het `data-src` kenmerk plaatsen. Stel vervolgens het bestaande `src` kenmerk zo in dat een 1x1 GIF-afbeelding wordt gecodeerd als Data URI. Hiermee vermindert u het aantal HTTP-aanvragen dat door de webpagina tijdens het laden wordt verzonden. Als SEO (zoekmachine optimaliseren) nodig is, is het echter beter om een `title` kenmerk voor de afbeeldingsinstantie in te stellen.

   Hieronder ziet u een voorbeeld van het definiëren van een `data-breakpoints` kenmerk voor de afbeelding en het gebruik van een GIF-code van 1 x 1 die is gecodeerd als Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Roep de `s7responsiveImage` API-functie aan voor elke afbeeldingsinstantie die in de bibliotheek wordt beheerd.

   Roep de `s7responsiveImage` API-functie aan voor elke afbeeldingsinstantie die in de bibliotheek wordt beheerd. Na een dergelijke aanroep vervangt de bibliotheek de oorspronkelijke afbeelding door de afbeelding die is gedownload van Image Serving, afhankelijk van de runtimegrootte van het `IMG` element in de webpaginalay-out en de schermdichtheid van het apparaat.

   De volgende code is een voorbeeld van het aanroepen van `s7responsiveImage` API-functie op een afbeelding, ervan uitgaande dat dit een id van die afbeelding `responsiveImage` is:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Voorbeeld {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

De bibliotheek ondersteunt het werken met veel afbeeldingsinstanties op de webpagina tegelijk. Herhaal daarom stap 1 en 2 hierboven voor elke afbeelding die u in de bibliotheek wilt beheren.

Het is de verantwoordelijkheid van de webpagina om het afbeeldingselement zodanig op te maken dat het flexibel van formaat is. In de bibliotheek met responsieve afbeeldingen zelf wordt geen onderscheid gemaakt tussen vaste en dynamische afbeeldingen. Als de afbeelding op een vaste grootte wordt toegepast, wordt de nieuwe afbeelding slechts eenmaal geladen.

De volgende code is een volledig voorbeeld van een triviale webpagina met één dynamische afbeelding die wordt beheerd door de bibliotheek Responsieve afbeelding. Het voorbeeld bevat extra CSS-stijlen om de afbeelding &quot;responsief&quot; te maken voor de venstergrootte van de webbrowser:

```
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Slim uitsnijden gebruiken**

Er zijn twee Slimme wijzen van het Gewas beschikbaar in AEM 6.4 en Kijkers Scene7 5.9:

* **Handmatig** - door de gebruiker gedefinieerde onderbrekingspunten en de bijbehorende opdrachten in de Image Service worden gedefinieerd binnen een kenmerk in het afbeeldingselement.
* **Slim uitsnijden** - berekende slimme uitsnijduitvoeringen worden automatisch opgehaald van de leveringsserver. De beste vertoning wordt geselecteerd gebruikend de runtime grootte van het beeldelement.

Als u de modus Slim uitsnijden wilt gebruiken, stelt u het `data-mode` kenmerk in op `smart crop`. Bijvoorbeeld:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Het gekoppelde afbeeldingselement verzendt een `s7responsiveViewer` gebeurtenis tijdens runtime wanneer het onderbrekingspunt verandert.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
