---
description: Hiermee verwijdert u een afbeelding met hyperlinks.
seo-description: Hiermee verwijdert u een afbeelding met hyperlinks.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Dynamic Media Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# deleteImageMap{#deleteimagemap}

Hiermee verwijdert u een afbeelding met hyperlinks.

Syntaxis

## Toegestane gebruikerstypen {#section-41fd188af16a40d4b07923165bcf15d8}

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
