---
description: Plaatst de toestemmingen van één enkel middel door een toestemmingsactiva te gebruiken.
seo-description: Plaatst de toestemmingen van één enkel middel door een toestemmingsactiva te gebruiken.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetPermissions{#setassetpermissions}

Plaatst de toestemmingen van één enkel middel door een toestemmingsactiva te gebruiken.

Elementen nemen standaard de machtigingen van hun bovenliggende map over. Nadat u machtigingen voor een element hebt ingesteld, worden de machtigingen van het bovenliggende element niet meer overgeërfd, tenzij u deze aanroept `removeAssetPermissions`.

## Geautoriseerde gebruikerstypen {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissionParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat de map bevat waarmee u wilt werken. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Mapgreep. |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | Ja | Machtigingenarray. |

**Output (setAssetPermissionReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-38955bc330bb4909b6b06027ef2b143e}

In dit codevoorbeeld worden machtigingen voor een element ingesteld. Het bevat het bedrijf en activa handvat, en een toestemmingenserie.

**Verzoek**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Antwoord**

Geen.
