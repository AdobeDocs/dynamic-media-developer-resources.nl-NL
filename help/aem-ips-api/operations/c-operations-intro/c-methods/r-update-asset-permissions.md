---
description: Werkt elementmachtigingen bij.
seo-description: Werkt elementmachtigingen bij.
seo-title: updateAssetPermission
solution: Experience Manager
title: updateAssetPermission
topic: Dynamic Media Image Production System API
uuid: feb2faf3-81de-436e-82de-1e41df03508f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---


# updateAssetPermission{#updateassetpermissons}

Werkt elementmachtigingen bij.

Syntaxis

## Toegestane gebruikerstypen {#section-3928e9badc3842e1859af4ed362df719}

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
