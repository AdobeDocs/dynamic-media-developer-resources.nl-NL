---
description: Mapmachtigingen bijwerken.
seo-description: Mapmachtigingen bijwerken.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateFolderPermissions{#updatefolderpermissions}

Mapmachtigingen bijwerken.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Mapgreep. |
| ` *`updateChildren`*` | `xsd:boolean` | Ja | Bepaalt of onderliggende items moeten worden bijgewerkt met de machtigingen die voor de map op het hoogste niveau zijn ingesteld. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | Ja | De array met machtigingsupdates die u wilt toepassen op de map. |

**Output (updateFolderPermissionsReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-c3fe4d4388674870a3856c35ef66b631}

**Verzoek**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Antwoord**

Geen.
