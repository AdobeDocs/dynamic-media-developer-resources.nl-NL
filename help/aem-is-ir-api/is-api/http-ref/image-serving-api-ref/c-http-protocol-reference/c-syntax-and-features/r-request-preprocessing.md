---
description: De Server van het beeld verstrekt een eenvoudig verzoek preprocessor die op regelmatige-uitdrukkingsgelijke en substitutieregels wordt gebaseerd.
seo-description: De Server van het beeld verstrekt een eenvoudig verzoek preprocessor die op regelmatige-uitdrukkingsgelijke en substitutieregels wordt gebaseerd.
seo-title: Voorbewerking aanvragen
solution: Experience Manager
title: Voorbewerking aanvragen
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Voorbewerking aanvragen{#request-preprocessing}

De Server van het beeld verstrekt een eenvoudig verzoek preprocessor die op regelmatige-uitdrukkingsgelijke en substitutieregels wordt gebaseerd.

U kunt verzamelingen regels (regelsets) koppelen aan elke afbeeldingscatalogus, inclusief de standaardcatalogus. Regels worden opgegeven bij bestanden met XML-opmaak.

De pre-verwerkingsregels van het verzoek kunnen de weg en vraaggedeelten verzoeken wijzigen alvorens zij door de parser van de Server van het Platform, met inbegrip van het manipuleren van de weg, het toevoegen van bevelen, het veranderen van bevelwaarden, en het toepassen van malplaatjes of macro&#39;s worden verwerkt. De regels kunnen ook worden gebruikt om bepaalde veiligheidseigenschappen te vormen en met voeten te treden die normaal slechts met catalogusattributen, zoals verzoekverwarring, water-markering, en het beperken van de dienst van HTTP tot specifieke cliëntIP adressen worden gecontroleerd.

Voorverwerkingsregels voor aanvragen zijn geschikt voor diverse toepassingen, waarvan sommige hieronder worden vermeld:

* Implementeer een *virtueel paden* mechanisme, waarmee het aanvraagpad opnieuw kan worden toegewezen aan bestands-, FTP- en HTTP-paden.
* Selectief afdwingen van beveiligingsfuncties, zoals watermerken, gefilterd op afbeeldingsnaam of pad.
* Watermerken of andere beveiligingsfuncties weglaten wanneer de server wordt benaderd vanuit specifieke IP-adressen.
* Het dwingen van toepassing van bevelen, zoals `defaultImage=`, op alle verzoeken of op verzoeken die een specifiek patroon in de weg URL of vraagkoorden tentoonstellen.
* Het gebruik van CPU-intensieve opdrachten om servermisbruik te voorkomen, wordt niet toegestaan.
* Het toestaan van bronbeelden om op de servers van HTTP of van FTP te worden gevestigd terwijl nog het specificeren van hen op de verzoekweg eerder dan met `src=`.
* De kwaliteitsinstellingen voor afbeeldingen bepalen (zoals JPEG-kwaliteit of verscherpen), afhankelijk van het aanvraagpad of de naam van de afbeelding.

Gedetailleerde informatie over het creëren van, het gebruiken van, en het beheren van regelreeksen kan in [Reeks van de Regel Verwijzing](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) worden gevonden.

## Zie ook {#see-also}

[Referentie](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) voor regelset,  [kenmerk::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
