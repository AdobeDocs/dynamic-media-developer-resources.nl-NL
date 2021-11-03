---
description: Viewer SDK-naamruimte
solution: Experience Manager
title: Viewer SDK-naamruimte
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: d1f12c9d-9b00-44ee-bd91-76a4d882fecf
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. In de meeste gevallen hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten; alle algemene behoeften worden gedekt door de viewer-API zelf.

Bij sommige geavanceerde gebruiksgevallen is het echter vereist dat de webpagina een verwijzing ophaalt naar een binnenste SDK-component met behulp van de `getComponent()` viewer-API en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruiken.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in AEM (Adobe Experience Manager), laadt de viewer SDK-componenten in `s7viewers.s7sdk` naamruimte. Op dezelfde manier laadt de viewer die vanuit Dynamic Media Classic wordt aangeboden de SDK in `s7classic.s7sdk`.

In beide gevallen heeft de naamruimte die wordt gebruikt door de SDK in de viewer `s7viewers` of `s7classic` als voorvoegsel. En het is anders dan de gewone `s7sdk` naamruimte die wordt gebruikt in de SDK User Guide of SDK API documentatie. Daarom is het belangrijk om een volledig gekwalificeerde SDK-naamruimte te gebruiken wanneer u aangepaste toepassingscode schrijft die communiceert met interne viewercomponenten.

Als u bijvoorbeeld wilt luisteren naar `StatusEvent.NOTF_VIEW_READY` en de viewer wordt bediend van AEM, is het volledig gekwalificeerde gebeurtenistype `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`en de gebeurtenislistenercode ziet er als volgt uit:

```
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
