---
description: Sjablonen kunnen worden gebruikt om de lengte en complexiteit te verminderen van aanvragen die meerdere afbeeldingslagen samenstellen of die tekst met RTF-indeling bevatten.
seo-description: Sjablonen kunnen worden gebruikt om de lengte en complexiteit te verminderen van aanvragen die meerdere afbeeldingslagen samenstellen of die tekst met RTF-indeling bevatten.
seo-title: Sjablonen
solution: Experience Manager
title: Sjablonen
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Sjablonen{#templates}

Sjablonen kunnen worden gebruikt om de lengte en complexiteit te verminderen van aanvragen die meerdere afbeeldingslagen samenstellen of die tekst met RTF-indeling bevatten.

Aangepaste variabelen kunnen worden gebruikt om het sjabloongebruik verder te vereenvoudigen. Sjablonen worden vaak zo ingesteld dat afbeeldingen of tekst eenvoudig kunnen worden gewisseld of dat andere opties tijdens runtime kunnen worden ingesteld.

Sjablonen worden opgeslagen als records in afbeeldingcatalogi, waarbij de hoofdtekst van de sjabloon in het `catalog::Modifier` veld wordt weergegeven en het `catalog::Path` veld leeg is of een statische achtergrondafbeelding opgeeft die niet dynamisch kan worden gewijzigd.

Sjablonen worden opgegeven met de `template=` opdracht of in de padcomponent van de aanvraag-URL. Voor de meeste toepassingen wordt aangeraden de `template=` opdracht te gebruiken om sjablonen op te geven. De `template=`opdracht mag niet in het `catalog::PostModifier` veld voorkomen en kan alleen in het `catalog::Modifier` veld in een geneste IS-aanvraag (d.w.z. in een `src=is{...}` constructie) plaatsvinden. Sjabloonrecords mogen niet worden vermeld in `src=` of `mask=`opdrachten.

Alle `src=` of `mask=`opdrachten die in de sjabloon zijn ingesloten, kunnen worden omgezet in de hoofdcatalogus van de aanvraag of in een andere afbeeldingscatalogus. Als er niet expliciet `rootId` is opgegeven, wordt de hoofdcatalogus aangenomen. De sjabloon die u opgeeft met `template=` kan zich ook in de hoofdcatalogus of in een andere afbeeldingscatalogus bevinden.

Het wordt ten zeerste aanbevolen om altijd standaarddefinities op te nemen voor alle variabelen die in een sjabloon worden gebruikt. Op deze manier kan de afbeeldingsuitvoer van de sjabloon altijd eenvoudig worden weergegeven door de grootte `attribute::RootId` en `catalog::Id`zonder dat u hoeft te weten welke variabelen in de sjabloon worden gebruikt.

De vooraf gedefinieerde padvervangingsvariabele `$object$` kan worden gebruikt om het afbeeldingsobject dat in het URL-pad is opgegeven, toe te passen op een laagbron of laagmasker ( `src=` of `mask=`), zelfs in geneste of ingesloten aanvragen.

* [Voorbeeld A](r-example-a.md)
* [Voorbeeld B](r-example-b.md)
* [Voorbeeld C](r-example-c.md)
