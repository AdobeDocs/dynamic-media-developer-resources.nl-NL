---
description: Viewer SDK-naamruimte
solution: Experience Manager
title: Viewer SDK-naamruimte
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Ontwikkelaar,zakelijke praktiserer
exl-id: 1712f08c-70e6-483e-a4e5-614448f35374
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Viewer SDK-naamruimte{#viewer-sdk-namespace}

De viewer is samengesteld uit veel Viewer SDK-componenten. In de meeste gevallen hoeft de webpagina niet rechtstreeks te communiceren met de API voor SDK-componenten; alle algemene behoeften worden gedekt door de viewer-API zelf.

Sommige gevallen van geavanceerd gebruik vereisen echter dat de webpagina een verwijzing ophaalt naar een binnenste SDK-component met de viewer-API `getComponent()` en vervolgens alle flexibiliteit van de API&#39;s van SDK zelf gebruikt.

De naamruimte die door de viewer wordt gebruikt voor het laden en initialiseren van SDK-componenten, is afhankelijk van de omgeving waarin de viewer werkt. Als de viewer wordt uitgevoerd in AEM (Adobe Experience Manager), laadt de viewer SDK-componenten in de naamruimte `s7viewers.s7sdk`. En de viewer die vanuit Dynamic Media Classic wordt aangeboden, laadt de SDK in `s7classic.s7sdk`.

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
