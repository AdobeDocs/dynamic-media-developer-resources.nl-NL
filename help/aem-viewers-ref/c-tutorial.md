---
title: Zelfstudie voor viewer-SDK
description: De Viewer SDK bevat een set JavaScript-componenten voor de ontwikkeling van aangepaste viewers. De viewers zijn webtoepassingen waarmee rich media-inhoud van Adobe Dynamic Media kan worden ingesloten in webpagina's.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Zelfstudie voor viewer-SDK{#viewer-sdk-tutorial}

De Viewer SDK bevat een set JavaScript-componenten voor de ontwikkeling van aangepaste viewers. De viewers zijn webtoepassingen waarmee rich media-inhoud van Adobe Dynamic Media kan worden ingesloten in webpagina&#39;s.

De SDK biedt bijvoorbeeld interactief zoomen en pannen. Het biedt ook een weergave van 360° en het afspelen van video&#39;s van elementen die via de back-end toepassing Dynamic Media Classic naar Adobe Dynamic Media zijn geüpload.

Hoewel de componenten afhankelijk zijn van de HTML5-functionaliteit, zijn ze ontworpen om te werken op Android™- en Apple iOS-apparaten en desktops, waaronder Internet Explorer en hoger. Dit soort ervaring betekent dat u één workflow kunt bieden voor alle ondersteunde platforms.

De SDK bestaat uit UI-componenten waaruit viewerinhoud bestaat. U kunt deze componenten opmaken via CSS en niet-UI-componenten die een ondersteunende rol hebben, zoals het ophalen en parseren of bijhouden van definities. Alle componentgedragingen zijn aanpasbaar via wijzigingstoetsen die u op verschillende manieren kunt opgeven, bijvoorbeeld `name=value` paren in de URL.

Deze zelfstudie bevat de volgende taakvolgorde om u te helpen een standaardzoomviewer te maken:

* [Download de nieuwste Viewer SDK van Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [De SDK van de viewer laden](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Stijl toevoegen aan uw viewer](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Inclusief container en ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Componenten MediaSet en Stalen toevoegen aan uw viewer](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Knoppen toevoegen aan uw viewer](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [De stalen verticaal configureren](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Download de nieuwste Viewer SDK van Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Download de nieuwste Viewer SDK van Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >U kunt deze zelfstudie voltooien zonder dat u het pakket met de Viewer SDK hoeft te downloaden omdat de SDK extern is geladen. Het Viewer-pakket bevat echter aanvullende voorbeelden en een API-naslaggids die u kan helpen uw eigen viewers te maken.

## De SDK van de viewer laden {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Maak eerst een nieuwe pagina voor de ontwikkeling van de standaardzoomviewer die u gaat maken.

   Bekijk deze nieuwe pagina met de Bootstrap- of loader-code die u gebruikt om een lege SDK-toepassing in te stellen. Open uw favoriete tekstverwerker en plak de volgende HTML-opmaakcode in deze editor:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   Voeg de volgende JavaScript-code toe in de `script` -tag wordt geïnitialiseerd `ParameterManager`. Zo kunt u zich voorbereiden op het maken en instantiëren van SDK-componenten in het dialoogvenster `initViewer` functie:

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. Sla het bestand op als een lege sjabloon. U kunt elke gewenste bestandsnaam gebruiken.

   U gebruikt dit lege sjabloonbestand als referentie wanneer u in de toekomst viewers maakt. Deze sjabloon werkt lokaal en vanaf een webserver.

Voeg nu stijl toe aan uw viewer.

## Stijl toevoegen aan uw viewer {#section-3783125360a1425eae5a5a334867cc32}

1. Voor deze viewer voor volledige pagina&#39;s die u maakt, kunt u enkele basisstijlen toevoegen.

   Voeg het volgende toe `style` van het blok aan de bodem van `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

Neem nu de componenten op `Container` en `ZoomView`.

## Inclusief container en ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Een werkelijke viewer maken door de componenten op te nemen `Container` en `ZoomView`.

   Het volgende invoegen `include` instructies onder aan het dialoogvenster `<head>` element—na het [!DNL Utils.js] script is geladen:

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Maak nu variabelen om te verwijzen naar de verschillende SDK-componenten.

   Voeg de volgende variabelen aan de bovenkant van de belangrijkste anonieme functie, enkel boven toe `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. Plaats het volgende in het dialoogvenster `initViewer` zodat u enkele modifiers kunt definiëren en de respectievelijke componenten kunt instantiëren:

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Voor een correcte uitvoering van de bovenstaande code voegt u een `containerResize` gebeurtenishandler en een hulpfunctie:

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. Geef een voorvertoning van de pagina weer, zodat u kunt zien wat u hebt gemaakt. De pagina moet er als volgt uitzien:

   ![Voorbeeld van één afbeelding](assets/viewer-1.jpg)

Voeg nu de componenten toe `MediaSet` en `Swatches` naar uw viewer.

## Componenten MediaSet en Stalen toevoegen aan uw viewer {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Als u gebruikers de mogelijkheid wilt geven om afbeeldingen uit een set te selecteren, kunt u de componenten toevoegen `MediaSet` en `Swatches`.

   Voeg de volgende SDK toe:

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Werk de lijst met variabelen als volgt bij:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. Instantiëren `MediaSet` en `Swatches` componenten binnen de `initViewer` functie.

   Instantieer de opdracht `Swatches` instantie na de `ZoomView` en `Container` de componenten, anders verbergt de het stapelen orde `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Voeg nu de volgende gebeurtenishandlerfuncties toe:

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. Plaats de stalen onder aan de viewer door de volgende CSS toe te voegen aan de `style` element:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Geef een voorvertoning van uw viewer weer.

   De stalen bevinden zich linksonder in de viewer. Als u wilt dat de stalen de volledige viewerbreedte beslaan, voegt u een aanroep toe om de stalen handmatig te vergroten of te verkleinen wanneer de gebruiker de grootte van de browser wijzigt. Voeg het volgende toe aan de `resizeViewer` functie:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   De viewer ziet er nu uit als de volgende afbeelding. Probeer het browservenster van de viewer aan te passen en bekijk het gedrag.

   ![Voorbeeld van viewer twee afbeeldingen](assets/viewer-2.jpg)

Voeg nu knoppen voor inzoomen, uitzoomen en het opnieuw instellen van zoomen toe aan uw viewer.

## Knoppen toevoegen aan uw viewer {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Op dit moment kan de gebruiker alleen zoomen met klik- of aanraakbewegingen. Voeg daarom enkele standaardknoppen voor zoomknoppen toe aan de viewer.

   Voeg de volgende knopcomponenten toe:

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Werk de lijst met variabelen als volgt bij:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Instantieknoppen onder aan `initViewer` functie.

   Onthoud dat de volgorde van belang is, tenzij u de optie `z-index` in CSS:

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Definieer nu enkele basisstijlen voor de knoppen door het volgende toe te voegen aan de knop `style` blok boven aan het bestand:

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. Geef een voorvertoning van uw viewer weer. Het zou als het volgende moeten kijken:

   ![Voorbeeld van viewer drie afbeeldingen](assets/viewer-3.jpg)

   Configureer nu de stalen, zodat deze verticaal aan de rechterkant worden uitgelijnd.

## De stalen verticaal configureren {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. U kunt wijzigingstoetsen op het `ParameterManager` -instantie.

   Voeg het volgende toe aan de bovenkant van `initViewer` zodat u de `Swatches` duimlay-out als één enkele rij:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Werk volgende resize vraag binnen bij `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. Het volgende bewerken `s7swatches` regel in `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Geef een voorvertoning van uw viewer weer. Het ziet er als volgt uit:

   ![Voorbeeld van viewer met vier afbeeldingen](assets/viewer-4.jpg)

   Uw standaardzoomviewer is nu voltooid.

   Deze viewerzelfstudie behandelt de grondbeginselen van wat de Dynamic Media Viewer SDK biedt. Terwijl u met de SDK werkt, kunt u de verschillende standaardcomponenten gebruiken om eenvoudig rijke kijkervaringen voor uw doelpubliek te maken en te stijlaliseren.
