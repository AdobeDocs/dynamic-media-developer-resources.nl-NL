---
title: De bibliotheek met responsieve afbeeldingen gebruiken
description: Voer de volgende stappen uit om een bibliotheek met responsieve afbeeldingen aan een webpagina toe te voegen en bestaande afbeeldingen met de bibliotheek te beheren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# De bibliotheek met responsieve afbeeldingen gebruiken{#using-responsive-image-library}

Voer de volgende stappen uit om een bibliotheek met responsieve afbeeldingen aan een webpagina toe te voegen en bestaande afbeeldingen met de bibliotheek te beheren.

**De bibliotheek met responsieve afbeeldingen gebruiken**

1. In Dynamic Media Classic: [een voorinstelling voor afbeeldingen maken](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html?lang=nl-NL#image-sizing) als u de bibliotheek met responsieve afbeeldingen wilt gebruiken met voorinstellingen.

   Als u voorinstellingen voor afbeeldingen definieert die worden gebruikt in de bibliotheek met responsieve afbeeldingen, mag u geen instellingen gebruiken die van invloed zijn op de afbeeldingsgrootte, zoals `wid=`, `hei=`, of `scl=`. Geef geen velden voor de grootte op in de voorinstelling Afbeelding. Laat ze in plaats daarvan leeg.
1. Voeg het JavaScript-bibliotheekbestand toe aan uw webpagina.

   Voordat u de API van de bibliotheek kunt gebruiken, moet u ervoor zorgen dat u `responsive_image.js`. Dit JavaScript-bestand bevindt zich in het dialoogvenster `libs/` submap van uw standaard IS-Viewers-implementatie:

   `<s7viewers_root>/libs/responsive_image.js`
1. Bestaande afbeeldingen instellen.

   De bibliotheek leest bepaalde configuratiekenmerken van een afbeeldingsinstantie waarmee het werkt. Kenmerken definiëren voor de `s7responsiveImage` API-functie wordt aangeroepen voor een dergelijke afbeelding.

   U kunt ook de bestaande afbeeldings-URL in het dialoogvenster `data-src` kenmerk. Stel vervolgens de bestaande `src` kenmerk voor het coderen van een afbeelding van een 1x1-GIF als Data URI. Hiermee vermindert u het aantal HTTP-aanvragen dat door de webpagina tijdens het laden wordt verzonden. Als SEO (zoekmachine optimaliseren) nodig is, is het echter beter om een `title` op de afbeeldingsinstantie.

   Hieronder ziet u een voorbeeld van het definiëren van `data-breakpoints` attribuut voor het beeld en het gebruiken van een 1x1 GIF dat als Gegevens URI wordt gecodeerd:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Roep de `s7responsiveImage` API-functie voor elke afbeeldingsinstantie die in de bibliotheek wordt beheerd.

   Roep de `s7responsiveImage` API-functie voor elke afbeeldingsinstantie die in de bibliotheek wordt beheerd. Na een dergelijke aanroep vervangt de bibliotheek de oorspronkelijke afbeelding door de afbeelding die is gedownload van Image Serving, afhankelijk van de runtimegrootte van de `IMG` -element in de webpaginalay-out en de schermdichtheid van het apparaat.

   De volgende code is een voorbeeld van het aanroepen van `s7responsiveImage` API-functie op een afbeelding, ervan uitgaande dat `responsiveImage` is een id van die afbeelding:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Voorbeeld {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

De bibliotheek ondersteunt het werken met veel afbeeldingsinstanties op de webpagina tegelijk. Herhaal daarom stap 1 en 2 hierboven voor elke afbeelding die u in de bibliotheek wilt beheren.

Het is de verantwoordelijkheid van de webpagina om het afbeeldingselement zodanig op te maken dat het flexibel van formaat is. In de bibliotheek met responsieve afbeeldingen zelf wordt geen onderscheid gemaakt tussen vaste en dynamische afbeeldingen. Als de afbeelding op een vaste grootte wordt toegepast, wordt de nieuwe afbeelding slechts eenmaal geladen.

De volgende code is een volledig voorbeeld van een triviale webpagina met één dynamische afbeelding die wordt beheerd door de bibliotheek Responsieve afbeelding. Het voorbeeld bevat extra CSS-stijlen om de afbeelding &quot;responsief&quot; te maken voor de venstergrootte van de webbrowser:

```html {.line-numbers}
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

Er zijn twee modi voor slim uitsnijden beschikbaar in AEM 6.4 en Dynamic Media Viewers 5.9:

* **Handmatig** - door de gebruiker gedefinieerde onderbrekingspunten en de bijbehorende opdrachten in Image Service worden gedefinieerd binnen een kenmerk in het afbeeldingselement.
* **Slim uitsnijden** - berekende slimme uitsnijdingen worden automatisch opgehaald van de leveringsserver. De beste vertoning wordt geselecteerd gebruikend de runtime grootte van het beeldelement.

Als u de modus Slim uitsnijden wilt gebruiken, stelt u de optie `data-mode` kenmerk naar `smart crop`. Bijvoorbeeld:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Het gekoppelde afbeeldingselement verzendt een `s7responsiveViewer` gebeurtenis tijdens runtime wanneer het onderbrekingspunt verandert.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
