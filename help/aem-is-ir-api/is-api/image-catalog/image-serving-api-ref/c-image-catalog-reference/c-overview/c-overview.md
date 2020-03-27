---
description: Afbeeldingscatalogi worden gebruikt om informatie over afbeeldingen en ondersteunende gegevens (zoals lettertypen en ICC-profielen) aan de server te verstrekken.
seo-description: Afbeeldingscatalogi worden gebruikt om informatie over afbeeldingen en ondersteunende gegevens (zoals lettertypen en ICC-profielen) aan de server te verstrekken.
seo-title: Overzicht
solution: Experience Manager
title: Overzicht
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Overzicht{#overview}

Afbeeldingscatalogi worden gebruikt om informatie over afbeeldingen en ondersteunende gegevens (zoals lettertypen en ICC-profielen) aan de server te verstrekken.

Afbeeldingscatalogi worden gebruikt om informatie over afbeeldingen en ondersteunende gegevens (zoals lettertypen en ICC-profielen) aan de server te verstrekken.

Elke afbeeldingscatalogus bestaat uit een vereist kenmerkbestand voor de catalogus en een set optionele bestanden met catalogusgegevens:

* Het afbeeldingsgegevensbestand waarin afbeeldingen en sjablonen en de bijbehorende metagegevens worden gespecificeerd.
* Het SVG-gegevensbestand waarin SVG-bestanden en de bijbehorende metagegevens worden vermeld.
* Het macro definitiedossier, dat definities voor verzoekmacro&#39;s verstrekt.
* Het bestand met lettertypetoewijzing, dat tekstlettertypen bijhoudt.
* Het profielkaartbestand, dat ICC-kleurprofielen opgeeft.
* Het bestand met regelsets waarin de regels voor voorbewerking van HTTP-aanvragen worden gedefinieerd.

De dossiers van de catalogusgegevens worden geassocieerd met beeldcatalogi door dossierverwijzingen in het dossier van de catalogusattributen. Hetzelfde bestand met catalogusgegevens kan worden gedeeld door meerdere afbeeldingscatalogi.

Bestanden met cataloguskenmerken moeten een [!DNL .ini] achtervoegsel hebben en moeten zich in de catalogusmap ( `PlatformServer::catalog.rootPath`) van de platformserver bevinden. Catalogusgegevensbestanden kunnen zich in dezelfde map of in een andere map bevinden die toegankelijk is voor de platformserver.

Dit document beschrijft het het dossierformaat van de Catalogus van het Beeld van het Beeld Scene7 voor het Serven systeem van het Beeld. Het beoogde publiek is ervaren programmeurs en ontwikkelaars van websites die Scene7 Image Serving voor een Web of een douanetoepassing willen gebruiken.

Men veronderstelt dat de lezer over het algemeen vertrouwd met het Beeld Scene7 die systeem, algemene het protocolnormen en overeenkomsten van HTTP, en basistafbeeldingsterminologie voert.
