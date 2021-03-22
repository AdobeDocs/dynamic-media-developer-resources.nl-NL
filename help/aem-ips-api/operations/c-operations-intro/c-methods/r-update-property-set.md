---
description: Gebruikt een bezitsserie om een bezitsreeks bij te werken.
seo-description: Gebruikt een bezitsserie om een bezitsreeks bij te werken.
seo-title: updatePropertySet
solution: Experience Manager
title: updatePropertySet
uuid: 21a59c5a-7799-4af6-ab9f-b0311f5f7254
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# updatePropertySet{#updatepropertyset}

Gebruikt een bezitsserie om een bezitsreeks bij te werken.

Syntaxis

## Toegestane gebruikerstypen {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Input (updatePropertySetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Ja | Handgreep aan de bezitsreeks. |
| `*`replaceProperties`*` | `xsd:string` | Nee | Stel in op `true` om eigenschappen te vervangen. |
| `*`propertyArray`*` | `types:PropertyArray` | Ja | Array met bijgewerkte eigenschappen voor de set eigenschappen. |

**Output (updatePropertySetReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Deze codesteekproef werkt een bezit bij dat met eigenschappen in de bezitsserie wordt geplaatst.

**Verzoek**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Antwoord**

Geen.
