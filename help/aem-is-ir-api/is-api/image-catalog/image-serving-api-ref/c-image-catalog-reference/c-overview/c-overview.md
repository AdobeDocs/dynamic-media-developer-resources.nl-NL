---
description: Afbeeldingscatalogi worden gebruikt om informatie over afbeeldingen en ondersteunende gegevens (zoals lettertypen en ICC-profielen) aan de server te verstrekken.
solution: Experience Manager
title: Overzicht
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

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

Bestanden met cataloguskenmerken moeten een [!DNL .ini]-achtervoegsel hebben en moeten zich in de catalogusmap van de server van het Platform ( `PlatformServer::catalog.rootPath`) bevinden. De dossiers van de catalogusgegevens kunnen in de zelfde omslag of een andere omslag worden gevestigd die voor de Server van het Platform toegankelijk is.

In dit document wordt de bestandsindeling Image Catalog beschreven voor het Dynamic Media Image Serving-systeem. Het beoogde publiek is ervaren programmeurs en ontwikkelaars van websites die Dynamic Media Image Serving willen gebruiken voor een web- of aangepaste toepassing.

Aangenomen wordt dat de lezer over het algemeen bekend is met het Dynamic Media Image Serving System, de algemene normen en conventies voor HTTP-protocollen en de basistechnologie voor beeldbewerking.
