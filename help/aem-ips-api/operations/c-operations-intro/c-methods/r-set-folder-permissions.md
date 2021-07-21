---
description: Stelt mapmachtigingen in.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setFolderPermissions{#setfolderpermissions}

Stelt mapmachtigingen in.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-2a41135054954396b40f1228f2e63b42}

**Input (setFolderPermissionsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`folderHandle`*` | `xsd:string` | Ja | Mapgreep. |
| `*`setChildren`*` | `xsd:boolean` | Ja | Hiermee stelt u machtigingen in voor onderliggende items die tot de map behoren. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | Ja | Machtigingenarray. |

**Output (setFolderPermissionsReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-01730da4be874553ab44e3241cdf6357}

Dit codevoorbeeld specificeert een bedrijfshandvat, een omslaghandvat, en een toestemmingsserie met gedetailleerde informatie over de omslag. Deze toepassing past dezelfde machtigingen toe op de onderliggende items van de bovenliggende map.

**Verzoek**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Antwoord**

Geen.
