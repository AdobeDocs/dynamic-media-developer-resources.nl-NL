---
title: Viewer SDK-naamruimte
description: Viewer SDK-naamruimte
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8e37bb60-c875-48d6-8c86-93aba7f50f74
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. Doorgaans hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten. alle algemene behoeften worden gedekt door de viewer-API zelf.

Sommige gevallen van geavanceerd gebruik vereisen echter dat de webpagina verwijst naar een binnenste SDK-component met de viewer-API `getComponent()` en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruikt.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in Adobe Experience Manager, laadt de viewer SDK-componenten in `s7viewers.s7sdk` naamruimte. En de viewer die vanuit Dynamic Media Classic wordt aangeboden, laadt de SDK in `s7classic.s7sdk`.

In beide gevallen heeft de naamruimte die door de SDK in de viewer wordt gebruikt `s7viewers` of `s7classic` als voorvoegsel. En de naamruimte verschilt van de naamruimte `s7sdk` die in de SDK User Guide of SDK API-documentatie wordt gebruikt.

Daarom is het belangrijk om een volledig gekwalificeerde SDK-naamruimte te gebruiken wanneer u aangepaste toepassingscode schrijft die communiceert met interne viewercomponenten.

Als u bijvoorbeeld naar de gebeurtenis `StatusEvent.NOTF_VIEW_READY` wilt luisteren en de viewer vanuit de Experience Manager wordt aangeboden, is het volledig gekwalificeerde gebeurtenistype `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` en ziet de gebeurtenislistenercode er ongeveer als volgt uit:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
