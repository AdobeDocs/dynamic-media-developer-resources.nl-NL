---
description: Een gebruiker van middelen en types in het systeem.
seo-description: Een gebruiker van middelen en types in het systeem.
seo-title: Gebruiker
solution: Experience Manager
title: Gebruiker
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# Gebruiker{#user}

Een gebruiker van middelen en types in het systeem.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Gebruikershandgreep. |
| ` *`firstName`*` | `xsd:string` | Voornaam gebruiker. |
| ` *`lastName`*` | `xsd:string` | Achternaam gebruiker. |
| ` *`email`*` | `xsd:string` | e-mailadres. |
| ` *`defaultRole`*` | `xsd:string` | Plaatst de rol voor een gebruiker in elk bedrijf zij tot behoren. Nochtans, treedt de gebruikersrol `IpsAmin` andere gebruikersrollen met voeten. |
| ` *`isValid`*` | `xsd:boolean` | Hiermee wordt bepaald of de gebruiker geldig is. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Hiermee stelt u de vervaldatum van het wachtwoord in. |

