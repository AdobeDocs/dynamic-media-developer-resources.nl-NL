---
description: De Server van het beeld verstrekt een eenvoudig verzoek preprocessor die op regelmatige-uitdrukkingsgelijke en substitutieregels wordt gebaseerd.
solution: Experience Manager
title: Voorbewerking aanvragen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Voorbewerking aanvragen{#request-preprocessing}

De Server van het beeld verstrekt een eenvoudig verzoek preprocessor die op regelmatige-uitdrukkingsgelijke en substitutieregels wordt gebaseerd.

U kunt verzamelingen regels (regelsets) koppelen aan elke afbeeldingscatalogus, inclusief de standaardcatalogus. Regels worden opgegeven bij bestanden met XML-opmaak.

De regels van de preprocessing van het verzoek kunnen de weg en vraaggedeelten van verzoeken wijzigen alvorens zij door worden verwerkt [!DNL Platform Server]De parser van de gebruiker, met inbegrip van het manipuleren van de weg, het toevoegen van bevelen, het veranderen van bevelwaarden, en het toepassen van malplaatjes of macro&#39;s. De regels kunnen ook worden gebruikt om bepaalde veiligheidseigenschappen te vormen en met voeten te treden die normaal slechts met catalogusattributen, zoals verzoekverwarring, water-markering, en het beperken van de dienst van HTTP tot specifieke cliëntIP adressen worden gecontroleerd.

Voorverwerkingsregels voor aanvragen zijn geschikt voor diverse toepassingen, waarvan sommige hieronder worden vermeld:

* Een *virtuele paden* mechanisme, waarmee het aanvraagpad opnieuw kan worden toegewezen aan bestands-, FTP- en HTTP-paden.
* Selectief afdwingen van beveiligingsfuncties, zoals watermerken, gefilterd op afbeeldingsnaam of pad.
* Watermerken of andere beveiligingsfuncties weglaten wanneer de server wordt benaderd vanuit specifieke IP-adressen.
* Het dwingen van toepassing van bevelen, zoals `defaultImage=`, aan alle verzoeken of aan verzoeken die een specifiek patroon in de weg URL of vraagkoorden tonen.
* Het gebruik van CPU-intensieve opdrachten om servermisbruik te voorkomen, wordt niet toegestaan.
* Bronafbeeldingen kunnen zich op HTTP- of FTP-servers bevinden terwijl ze nog steeds op het aanvraagpad worden opgegeven in plaats van met `src=`.
* De kwaliteitsinstellingen voor afbeeldingen bepalen (zoals de kwaliteit van de JPEG of de verscherping), afhankelijk van het aanvraagpad of de naam van de afbeelding.

Gedetailleerde informatie over het maken, gebruiken en beheren van regelsets vindt u in de [Verwijzing regelset](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Zie ook {#see-also}

[Verwijzing regelset](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [kenmerk::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
