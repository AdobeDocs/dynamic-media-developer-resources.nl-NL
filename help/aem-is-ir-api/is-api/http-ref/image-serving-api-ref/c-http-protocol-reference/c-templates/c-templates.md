---
title: Sjablonen
description: Sjablonen kunnen worden gebruikt om de lengte en complexiteit te verminderen van aanvragen die meerdere afbeeldingslagen samenstellen of die tekst met RTF-indeling bevatten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Sjablonen{#templates}

Sjablonen kunnen worden gebruikt om de lengte en complexiteit te verminderen van aanvragen die meerdere afbeeldingslagen samenstellen of die tekst met RTF-indeling bevatten.

Aangepaste variabelen kunnen worden gebruikt om het sjabloongebruik verder te vereenvoudigen. Sjablonen worden vaak zo ingesteld dat afbeeldingen of tekst eenvoudig kunnen worden gewisseld of dat andere opties tijdens runtime kunnen worden ingesteld.

Sjablonen worden opgeslagen als records in afbeeldingscatalogi, met de hoofdtekst van de sjabloon in het dialoogvenster `catalog::Modifier` en de `catalog::Path` veld leeg is of een statische achtergrondafbeelding opgeeft die niet dynamisch kan worden gewijzigd.

Sjablonen worden opgegeven met de `template=` of in de padcomponent van de aanvraag-URL. Voor de meeste toepassingen wordt aangeraden de opdracht `template=` gebruiken om sjablonen op te geven. De `template=`mag niet voorkomen in de `catalog::PostModifier` en kan alleen voorkomen in het veld `catalog::Modifier` veld in een geneste IS-aanvraag (d.w.z. in een `src=is{...}` construct). Er wordt mogelijk niet naar sjabloonrecords verwezen in `src=` of `mask=`opdrachten.

Alle `src=` of `mask=`opdrachten die zijn ingesloten in de sjabloon, worden mogelijk omgezet in de hoofdcatalogus van de aanvraag of in een andere afbeeldingscatalogus. Indien niet `rootId` expliciet wordt opgegeven, wordt de hoofdcatalogus aangenomen. De sjabloon die is opgegeven met `template=` kan zich ook in de hoofdcatalogus of een andere afbeeldingscatalogus bevinden.

Het wordt ten zeerste aanbevolen om altijd standaarddefinities op te nemen voor alle variabelen die in een sjabloon worden gebruikt. Op deze manier kan de uitgevoerde afbeelding van de sjabloon altijd eenvoudig worden weergegeven door de bijbehorende afbeelding op te geven `attribute::RootId` en `catalog::Id`, zonder te moeten weten welke variabelen in de sjabloon worden gebruikt.

De vooraf gedefinieerde variabele voor padvervanging `$object$` kan worden gebruikt om het afbeeldingsobject dat in het URL-pad is opgegeven, toe te passen op een willekeurige laagbron of een willekeurig laagmasker ( `src=` of `mask=`), zelfs in geneste of ingesloten aanvragen.

* [Voorbeeld A](r-example-a.md)
* [Voorbeeld B](r-example-b.md)
* [Voorbeeld C](r-example-c.md)
