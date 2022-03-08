---
description: Retourneert de leden van een groep.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# getGroupMembership{#getgroupmembership}

Retourneert de leden van een groep.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-35d070e5c4d74ca69df508368953cfb8}

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
| userHandle | `xsd:string` | Nee | De greep voor de gebruiker. |
| companyHandle | `xsd:string` | Nee | De handgreep aan het bedrijf. |

**Output (getGroupMembershipReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| groupArray | `types:GroupArray` | Ja | Array van groepen. |

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
