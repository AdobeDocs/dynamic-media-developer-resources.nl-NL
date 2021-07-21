---
description: Een map naar een nieuwe locatie verplaatsen.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# moveFolder{#movefolder}

Een map naar een nieuwe locatie verplaatsen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-7f1979fb5e504bdea3a8df01101b50c3}

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
