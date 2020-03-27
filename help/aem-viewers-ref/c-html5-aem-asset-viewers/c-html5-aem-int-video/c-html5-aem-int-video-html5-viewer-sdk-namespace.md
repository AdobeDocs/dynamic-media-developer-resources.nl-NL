---
description: 'null'
seo-description: 'null'
seo-title: Viewer SDK-naamruimte
solution: Experience Manager
title: Viewer SDK-naamruimte
topic: Dynamic media
uuid: 8c93bf01-0568-48fe-9083-1e85ba1549ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. In de meeste gevallen hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten; alle algemene behoeften worden gedekt door de viewer-API zelf.

Sommige gevallen van geavanceerd gebruik vereisen echter dat de webpagina een verwijzing ophaalt naar een binnenste SDK-component met behulp van de `getComponent()` viewer-API en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruikt.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in AEM (Adobe Experience Manager), laadt de viewer SDK-componenten in `s7viewers.s7sdk` naamruimte. Eveneens, laadt de kijker die van het Publiceren Scene7 Systeem wordt gediend SDK in `s7classic.s7sdk`.

In beide gevallen heeft de naamruimte die door de SDK in de viewer wordt gebruikt, het voorvoegsel `s7viewers` of `s7classic` . En deze is anders dan de naamruimte zonder opmaak die wordt gebruikt in de SDK User Guide of SDK API documentatie. `s7sdk`

Daarom is het belangrijk om een volledig gekwalificeerde SDK-naamruimte te gebruiken wanneer u aangepaste toepassingscode schrijft die communiceert met interne viewercomponenten.

Als u bijvoorbeeld naar de `StatusEvent.NOTF_VIEW_READY` gebeurtenis wilt luisteren en de viewer via AEM wordt aangeboden, is het volledig gekwalificeerde gebeurtenistype `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`en ziet de gebeurtenislistenercode er ongeveer als volgt uit:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

