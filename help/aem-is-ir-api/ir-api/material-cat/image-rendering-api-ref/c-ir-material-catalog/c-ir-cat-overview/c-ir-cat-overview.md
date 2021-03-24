---
description: Materiaalcatalogi bieden informatie over vignetten, materialen en ondersteunende gegevens, zoals ICC-profielen, aan de server.
solution: Experience Manager
title: Overzicht van de materiaalcatalogus *
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Overzicht materiaalcatalogus *{#material-catalog-overview}

Materiaalcatalogi bieden informatie over vignetten, materialen en ondersteunende gegevens, zoals ICC-profielen, aan de server.

Elke materiaalcatalogus bestaat uit een vereist *cataloguskenmerkbestand* en een set optionele *catalogusgegevensbestanden*:

* Het bestand met de vignettoewijzing waarin vignetten en sjablonen en de bijbehorende metagegevens worden beschreven.
* Het materiaalgegevensbestand, waarin materialen worden gespecificeerd en de bijbehorende bestanden en metagegevens voor structuurafbeeldingen worden aangegeven.
* Het macro definitiedossier, dat definities voor verzoekmacro&#39;s verstrekt.
* Het profielkaartbestand, dat ICC-kleurprofielen opgeeft.

De dossiers van de catalogusgegevens worden geassocieerd met materiaalcatalogi door dossierverwijzingen in het dossier van de catalogusattributen. Hetzelfde bestand met catalogusgegevens kan door meerdere materiaalcatalogi worden gedeeld.

Bestanden met cataloguskenmerken moeten een [!DNL .ini]-achtervoegsel hebben en moeten zich in de map *Catalogusmap* ( [!DNL PlatformServer::ir.catalogRootPath]) bevinden. Catalogusgegevensbestanden kunnen zich in dezelfde map of in een andere map bevinden die toegankelijk is voor de renderserver.

**Materiaalcatalogi bijwerken**

De server bewaakt voortdurend de catalogusmap en laadt automatisch een materiaalcatalogus, inclusief de bijbehorende bestanden met catalogusgegevens, wanneer wordt vastgesteld dat het hoofdbestand met cataloguskenmerken is gewijzigd. Als u dus materiaalcatalogi op de server wilt bijwerken, vervangt u eerst alle catalogusgegevensbestanden die moeten worden gewijzigd en vervangt u vervolgens het bestand met cataloguskenmerken (of &quot;aanraken&quot;) om het opnieuw laden van de catalogus te starten.

**Standaardcatalogus**

De standaardcatalogus bevat standaardwaarden voor alle cataloguskenmerken van alle materiaalcatalogi. Als een bepaald kenmerk niet in een specifieke materiaalcatalogus kan worden gevonden, gebruikt de server in plaats daarvan de bijbehorende waarde uit de standaardcatalogus. Op dezelfde manier kan de standaardcatalogus worden gebruikt om standaardwaarden op te geven voor specifieke records met catalogusgegevens (materialen en ICC-profielen). Als een bepaalde gegevensrecord niet kan worden gevonden in een specifieke materiaalcatalogus, probeert de server deze in plaats daarvan te vinden in de standaardcatalogus. Zo kunnen materiaalcatalogi dunbevolkt worden en wordt het beheer van algemene kenmerken en gegevens, zoals gedeelde sjablonen, macro&#39;s, lettertypen, enz., vereenvoudigd.

Bovendien bevat de standaardcatalogus alle kenmerken en gegevensrecords (ICC-profielen) wanneer een bewerking geen specifieke materiaalcatalogus bevat.

Voor een correcte werking van de Render-server moet het bestand met cataloguskenmerken voor de standaardcatalogus de naam [!DNL default.ini] hebben, altijd bestaan in de catalogusmap en moet het volledig zijn gevuld met alle vereiste kenmerken, met uitzondering van `attribute::RootId` en de verwijzingen naar de verschillende bestanden met catalogusgegevens, die allemaal optioneel zijn.

**Zie ook**

`PlatformServer::ir.catalogRootPath`
