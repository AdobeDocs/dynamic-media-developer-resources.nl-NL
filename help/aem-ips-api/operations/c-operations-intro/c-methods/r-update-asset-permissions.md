---
description: Werkt elementmachtigingen bij.
solution: Experience Manager
title: updateAssetPermission
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# updateAssetPermission{#updateassetpermissons}

Werkt elementmachtigingen bij.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-392cb3076cf84790a32fd913f2b111a3}

**Input (updateAssetPermissionsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset handle. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Ja | Machtigingen die u op het element wilt toepassen. |

**Output (updateAssetPermissionsReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Verzoek**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Antwoord**

Geen.
