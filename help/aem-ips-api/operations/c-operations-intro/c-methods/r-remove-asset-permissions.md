---
description: Verwijdert machtigingen uit geselecteerde elementen.
seo-description: Verwijdert machtigingen uit geselecteerde elementen.
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# removeAssetPermissions{#removeassetpermissions}

Verwijdert machtigingen uit geselecteerde elementen.

Syntaxis

## Toegestane gebruikerstypen {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Input (removeAssetPermissionsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep van het middel met toestemmingen u wilt verwijderen. |

**Output (removeAssetPermissionsReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-238fa7bb091548f5ba72ced11fc92d4f}

Dit codevoorbeeld verwijdert toestemmingen uit een middel.

**Verzoek**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Antwoord**

Geen.
