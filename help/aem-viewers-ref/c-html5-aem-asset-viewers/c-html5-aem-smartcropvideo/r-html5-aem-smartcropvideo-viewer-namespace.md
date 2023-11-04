---
title: Viewer SDK-naamruimte
description: Viewer SDK-naamruimte
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. Doorgaans hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten. Alle algemene behoeften worden behandeld in de viewer-API zelf.

Bij sommige gevallen van geavanceerd gebruik is het echter vereist dat de webpagina verwijst naar een binnenste SDK-component die de opdracht `getComponent()` viewer-API en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruiken.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in Adobe Experience Manager, laadt de viewer SDK-componenten in `s7viewers.s7sdk` naamruimte. Op dezelfde manier laadt de viewer die vanuit Dynamic Media Classic wordt aangeboden de SDK in `s7classic.s7sdk`.

In beide gevallen heeft de naamruimte die wordt gebruikt door de SDK in de viewer `s7viewers` of `s7classic` als prefix. En het is anders dan de gewone `s7sdk` naamruimte die wordt gebruikt in de SDK User Guide of SDK API documentatie. Daarom is het belangrijk om een volledig gekwalificeerde SDK-naamruimte te gebruiken wanneer u aangepaste toepassingscode schrijft die communiceert met interne viewercomponenten.

Als u bijvoorbeeld wilt luisteren naar `StatusEvent.NOTF_VIEW_READY` gebeurtenis en de viewer wordt aangeboden vanuit de Experience Manager, is het volledig gekwalificeerde gebeurtenistype `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`en de gebeurtenislistenercode ziet er als volgt uit:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
