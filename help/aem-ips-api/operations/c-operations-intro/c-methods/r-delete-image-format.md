---
description: Hiermee verwijdert u een afbeeldingsindeling. Haal de formaatgreep van de afbeelding op uit saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# deleteImageFormat{#deleteimageformat}

Hiermee verwijdert u een afbeeldingsindeling. Haal de formaatgreep van de afbeelding op uit saveImageFormat.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-462c05d9aad746ee8d2be0656041b693}

**Input (deleteImageFormatParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep naar het bedrijf dat de afbeeldingsindeling bevat die u wilt verwijderen. |
| imageFormatHandle | `xsd:string` | Ja | De handgreep naar de afbeeldingsindeling die u wilt verwijderen. |

**Output (deleteImageFormatParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

In dit codevoorbeeld wordt een afbeeldingsindeling van een bedrijf verwijderd. Haal de greep voor de afbeeldingsindeling op van een andere bewerking.

**Verzoek**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Antwoord**

Geen.

**Verwante onderwerpen:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
