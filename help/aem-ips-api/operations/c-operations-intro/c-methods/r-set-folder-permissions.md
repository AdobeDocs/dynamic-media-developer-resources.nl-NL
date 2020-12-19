---
description: Stelt mapmachtigingen in.
seo-description: Stelt mapmachtigingen in.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# setFolderPermissions{#setfolderpermissions}

Stelt mapmachtigingen in.

Syntaxis

## Toegestane gebruikerstypen {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-2a41135054954396b40f1228f2e63b42}

**Input (setFolderPermissionsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Mapgreep. |
| ` *`setChildren`*` | `xsd:boolean` | Ja | Hiermee stelt u machtigingen in voor onderliggende items die tot de map behoren. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` | Ja | Machtigingenarray. |

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
