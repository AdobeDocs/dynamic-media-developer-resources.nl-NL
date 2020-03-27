---
description: Bij het renderen van afbeeldingen worden materialen toegepast op groepen of objecten in vignetten.
seo-description: Bij het renderen van afbeeldingen worden materialen toegepast op groepen of objecten in vignetten.
seo-title: Materialen
solution: Experience Manager
title: Materialen
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# Materialen{#materials}

Bij het renderen van afbeeldingen worden materialen toegepast op groepen of objecten in vignetten.

Een materiaal bestaat uit een reeks *kenmerken*. Bepaalde kenmerken zijn vereist voor bepaalde materialen, andere zijn optioneel en andere worden genegeerd, indien aanwezig. Veel kenmerken hebben standaardwaarden. Niet alle materialen kunnen op alle objecten worden toegepast (een kast kan bijvoorbeeld niet op een bank worden aangebracht).

Om het even welke attributen die binnen een Segment van de Specificatie van het Materiaal voorkomen (MSS) maar niet hierboven of in de specifieke materiaallijsten hieronder vermeld zijn worden genegeerd door de server.

In de volgende tabellen worden de elementaire materiaalkenmerken weergegeven. IR steunt extra attributen voor het controleren van [geavanceerde teruggevende gevolgen](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Tenzij anders vermeld, zijn alle materiaalkenmerken optioneel, met geschikte standaardwaarden.

* [Effen kleuren](r-ir-solid-colors.md)
* [Herhaalbare structuren](r-ir-repeatable-textures.md)
* [Muurgrenzen](r-ir-wall-borders.md)
* [Decals](r-ir-decals.md)
* [Cabinetten](r-ir-cabinets.md)
* [Vensterbedekkingen](r-ir-window-coverings.md)
