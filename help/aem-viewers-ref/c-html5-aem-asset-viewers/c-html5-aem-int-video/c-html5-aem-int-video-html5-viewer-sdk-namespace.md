---
title: Viewer SDK-naamruimte
description: Viewer SDK-naamruimte
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 4a4d821e-9351-4efa-8849-968e746911f3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. Doorgaans hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten. alle algemene behoeften worden gedekt door de viewer-API zelf.

Bij sommige gevallen van geavanceerd gebruik is het echter vereist dat de webpagina verwijst naar een binnenste SDK-component die de opdracht `getComponent()` viewer-API en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruiken.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in Adobe Experience Manager, laadt de viewer SDK-componenten in `s7viewers.s7sdk` naamruimte. Op dezelfde manier laadt de viewer die vanuit Dynamic Media Classic wordt aangeboden de SDK in `s7classic.s7sdk`.

In beide gevallen heeft de naamruimte die wordt gebruikt door de SDK in de viewer `s7viewers` of `s7classic` als voorvoegsel. En het is anders dan de gewone `s7sdk` naamruimte die wordt gebruikt in de SDK User Guide of SDK API documentatie.

Daarom is het belangrijk om een volledig gekwalificeerde SDK-naamruimte te gebruiken wanneer u aangepaste toepassingscode schrijft die communiceert met interne viewercomponenten.

Als u bijvoorbeeld wilt luisteren naar `StatusEvent.NOTF_VIEW_READY` gebeurtenis en de viewer wordt aangeboden vanuit de Experience Manager, is het volledig gekwalificeerde gebeurtenistype `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`en de gebeurtenislistenercode ziet er als volgt uit:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
