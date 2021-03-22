---
description: Een map naar een nieuwe locatie verplaatsen.
seo-description: Een map naar een nieuwe locatie verplaatsen.
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# moveFolder{#movefolder}

Een map naar een nieuwe locatie verplaatsen.

Syntaxis

## Toegestane gebruikerstypen {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Input (moveFolderParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`folderHandle`*` | `xsd:string` | Ja | Mapgreep. |
| `*`destFolderHandle`*` | `xsd:string` | Ja | Handgreep aan de bestemmingsomslag. |

**Output (moveFolderReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Ja | Verwerk de verplaatste map. |

## Voorbeelden {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Verzoek**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Antwoord**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

