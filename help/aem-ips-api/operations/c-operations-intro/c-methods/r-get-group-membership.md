---
description: Retourneert de leden van een groep.
seo-description: Retourneert de leden van een groep.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Dynamic Media Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# getGroupMembership{#getgroupmembership}

Retourneert de leden van een groep.

Syntaxis

## Toegestane gebruikerstypen {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-2e92f850254e46e48403acaa215341a5}

**Input (getGroupMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nee | De greep voor de gebruiker. |
| `*`companyHandle`*` | `xsd:string` | Nee | De handgreep aan het bedrijf. |

**Output (getGroupMembershipReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Ja | Array van groepen. |

## Voorbeelden {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Deze codesteekproef keert alle leden van een groep terug. Omdat het bedrijf en de gebruikershandvatten facultatief zijn, kan de verrichting alle leden van alle groepen terugkeren.

**Verzoek**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Antwoord**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

