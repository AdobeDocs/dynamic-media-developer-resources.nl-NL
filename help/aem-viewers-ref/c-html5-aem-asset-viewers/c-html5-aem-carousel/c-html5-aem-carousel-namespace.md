---
description: Viewer SDK-naamruimte
solution: Experience Manager
title: Viewer SDK-naamruimte
topic: Dynamic Media
uuid: 993547f2-b943-4aba-b6cc-54fa32cfb2d3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. In de meeste gevallen hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten; alle algemene behoeften worden gedekt door de viewer-API zelf.

Sommige gevallen van geavanceerd gebruik vereisen echter dat de webpagina een verwijzing ophaalt naar een binnenste SDK-component met de viewer-API `getComponent()` en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruikt.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in AEM (Adobe Experience Manager), laadt de viewer SDK-componenten in de naamruimte `s7viewers.s7sdk`. En de viewer die wordt aangeboden via het Scene7 Publishing System laadt de SDK in `s7classic.s7sdk`.

In beide gevallen heeft de naamruimte die door de SDK in de viewer wordt gebruikt `s7viewers` of `s7classic` als voorvoegsel. En de naamruimte verschilt van de naamruimte `s7sdk` die in de SDK User Guide of SDK API-documentatie wordt gebruikt.

Daarom is het belangrijk om een volledig gekwalificeerde SDK-naamruimte te gebruiken wanneer u aangepaste toepassingscode schrijft die communiceert met interne viewercomponenten.

Als u bijvoorbeeld naar de gebeurtenis `StatusEvent.NOTF_VIEW_READY` wilt luisteren en de viewer vanuit AEM wordt bediend, is het volledig gekwalificeerde gebeurtenistype `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` en ziet de gebeurtenislistenercode er ongeveer als volgt uit:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

