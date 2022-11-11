---
description: Een gebruiker van middelen en types in het systeem.
solution: Experience Manager
title: Gebruiker
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# [!DNL User]{#user}

Een gebruiker van middelen en types in het systeem.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| userHandle | `xsd:string` | Gebruikershandgreep. |
| firstName | `xsd:string` | Voornaam gebruiker. |
| lastName | `xsd:string` | Achternaam gebruiker. |
| email | `xsd:string` | e-mailadres. |
| defaultRole | `xsd:string` | Plaatst de rol voor een gebruiker in elk bedrijf zij tot behoren. De gebruikersrol `IpsAmin` Hiermee overschrijft u andere gebruikersrollen. |
| isValid | `xsd:boolean` | Hiermee wordt bepaald of de gebruiker geldig is. |
| passwordExpires | `xsd:dateTime` | Hiermee stelt u de vervaldatum van het wachtwoord in. |
