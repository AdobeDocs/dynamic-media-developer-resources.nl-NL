---
description: Hiermee verwijdert u een afbeelding met hyperlinks.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# deleteImageMap{#deleteimagemap}

Hiermee verwijdert u een afbeelding met hyperlinks.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang tot het element hebben.

## Parameters {#section-28de12bab79045a5977c68855e37ae3d}

**Input (deleteImageMapParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf dat de te verwijderen afbeelding met hyperlinks bevat. |
| `*`imageMapHandle`*` | `xsd:string` | Ja | De handgreep van de afbeeldingskaart die moet worden verwijderd. |

**Output (deleteImageMapParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

In dit codevoorbeeld wordt een afbeelding met hyperlinks van een bedrijf verwijderd. U moet de handgreep voor de afbeelding met hyperlinks van een andere bewerking verkrijgen.

**Verzoek**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Antwoord**

Geen
