---
title: Overzicht van de materiaalcatalogus
description: Materiaalcatalogi bieden informatie over vignetten, materialen en ondersteunende gegevens, zoals ICC-profielen, aan de server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Overzicht van de materiaalcatalogus{#material-catalog-overview}

Materiaalcatalogi bieden informatie over vignetten, materialen en ondersteunende gegevens, zoals ICC-profielen, aan de server.

Elke materiaalcatalogus bestaat uit een vereiste *cataloguskenmerkbestand* en een set facultatieve *catalogusgegevensbestanden*:

* Het bestand met de vignettoewijzing waarin vignetten en sjablonen en de bijbehorende metagegevens worden beschreven.
* Het materiaalgegevensbestand, waarin materialen worden gespecificeerd en de bijbehorende bestanden en metagegevens voor structuurafbeeldingen worden aangegeven.
* Het macro definitiedossier, dat definities voor verzoekmacro&#39;s verstrekt.
* Het profielkaartbestand, dat ICC-kleurprofielen opgeeft.

De dossiers van de catalogusgegevens worden geassocieerd met materiaalcatalogi door dossierverwijzingen in het dossier van de catalogusattributen. Hetzelfde bestand met catalogusgegevens kan door meerdere materiaalcatalogi worden gedeeld.

Kenmerkbestanden van catalogus moeten een [!DNL `.ini`] bestandsachtervoegsel en moet in de renderfunctie voor afbeeldingen staan *catalogusmap* ( [!DNL PlatformServer::ir.catalogRootPath]). Catalogusgegevensbestanden kunnen zich in dezelfde map bevinden of in elke andere map die toegankelijk is voor de renderserver.

**Materiaalcatalogi bijwerken**

De server controleert de catalogusmap voortdurend. Er wordt automatisch een materiaalcatalogus opnieuw geladen, inclusief de bijbehorende bestanden met catalogusgegevens, wanneer wordt vastgesteld dat het hoofdbestand met cataloguskenmerken is gewijzigd. Als u dus materiaalcatalogi op de server wilt bijwerken, vervangt u eerst alle catalogusgegevensbestanden die moeten worden gewijzigd en vervangt u vervolgens het bestand met cataloguskenmerken (of &quot;aanraken&quot;) om het opnieuw laden van de catalogus te starten.

**Standaardcatalogus**

De standaardcatalogus bevat standaardwaarden voor alle cataloguskenmerken van alle materiaalcatalogi. Als een bepaald kenmerk niet in een specifieke materiaalcatalogus kan worden gevonden, gebruikt de server in plaats daarvan de corresponderende waarde uit de standaardcatalogus. Op dezelfde manier kan de standaardcatalogus worden gebruikt om standaardwaarden op te geven voor specifieke records met catalogusgegevens (materialen en ICC-profielen). Als een bepaalde gegevensrecord niet kan worden gevonden in een specifieke materiaalcatalogus, probeert de server deze in plaats daarvan te vinden in de standaardcatalogus. Hierdoor kunnen materiaalcatalogi dunbevolkt worden en wordt het beheer van algemene kenmerken en gegevens, zoals gedeelde sjablonen, macro&#39;s en lettertypen, vereenvoudigd.

Bovendien bevat de standaardcatalogus alle kenmerken en gegevensrecords (ICC-profielen) wanneer een bewerking geen specifieke materiaalcatalogus bevat.

Voor een correcte werking van de Render-server moet het bestand met cataloguskenmerken voor de standaardcatalogus een naam hebben [!DNL default.ini]. De catalogus moet ook altijd in de catalogusmap staan en moet volledig zijn gevuld met alle vereiste kenmerken, exclusief `attribute::RootId` en de verwijzingen naar de verschillende dossiers van catalogusgegevens, die allen facultatief zijn.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
