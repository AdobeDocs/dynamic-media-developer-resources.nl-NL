---
description: Retourneert bedrijfsgroepen.
solution: Experience Manager
title: getgroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# getgroups{#getgroups}

Retourneert bedrijfsgroepen.

Syntaxis

## Toegestane gebruikerstypen {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-0e06195f23dd4c69922df210f566dd18}

**Input (getgroupsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |

**Output (getgroupsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Ja | Array van groepen. |

## Voorbeelden {#section-ed0708f611574354bf0c6ea83912b531}

Deze code keert een serie terug die alle groepen bevat die tot een specifiek bedrijf en specifieke informatie over elke groep behoren.

**Verzoek**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```

