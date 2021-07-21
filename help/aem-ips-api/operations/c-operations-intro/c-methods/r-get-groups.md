---
description: Retourneert bedrijfsgroepen.
solution: Experience Manager
title: getgroups
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# getgroups{#getgroups}

Retourneert bedrijfsgroepen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

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
