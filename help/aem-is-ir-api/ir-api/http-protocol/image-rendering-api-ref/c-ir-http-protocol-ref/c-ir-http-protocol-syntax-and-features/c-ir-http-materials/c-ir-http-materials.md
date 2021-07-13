---
description: Bij het renderen van afbeeldingen worden materialen toegepast op groepen of objecten in vignetten.
solution: Experience Manager
title: Materialen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Materialen{#materials}

Bij het renderen van afbeeldingen worden materialen toegepast op groepen of objecten in vignetten.

Een materiaal bestaat uit een set *kenmerken*. Bepaalde kenmerken zijn vereist voor bepaalde materialen, andere zijn optioneel en andere worden genegeerd, indien aanwezig. Veel kenmerken hebben standaardwaarden. Niet alle materialen kunnen op alle objecten worden toegepast (een kast kan bijvoorbeeld niet op een bank worden aangebracht).

Om het even welke attributen die binnen een Segment van de Specificatie van het Materiaal voorkomen (MSS) maar niet hierboven of in de specifieke materiaallijsten hieronder vermeld zijn worden genegeerd door de server.

In de volgende tabellen worden de elementaire materiaalkenmerken weergegeven. IR steunt extra attributen voor het controleren [geavanceerde teruggeeft gevolgen](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Tenzij anders vermeld, zijn alle materiaalkenmerken optioneel, met geschikte standaardwaarden.

* [Effen kleuren](r-ir-solid-colors.md)
* [Herhaalbare structuren](r-ir-repeatable-textures.md)
* [Muurgrenzen](r-ir-wall-borders.md)
* [Decals](r-ir-decals.md)
* [Cabinetten](r-ir-cabinets.md)
* [Vensterbedekkingen](r-ir-window-coverings.md)
