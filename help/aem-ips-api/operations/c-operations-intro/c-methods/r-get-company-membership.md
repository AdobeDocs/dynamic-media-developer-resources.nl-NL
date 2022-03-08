---
description: Haalt de lidmaatschappen van een gebruiker in een bedrijfserie op.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# getCompanyMembership{#getcompanymembership}

Haalt de lidmaatschappen van een gebruiker in een bedrijfserie op.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Input (getCompanyMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userHandle | `xsd:string` | Nee | De handgreep aan de gebruiker van wie lidmaatschap u wilt verkrijgen. |

**Output (getCompanyMembershipReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| membershipArray | `types:CompanyMembershipArray` | Ja | Array van lidmaatschap van bedrijven. |

## Voorbeelden {#section-e4958d104ea344a4a79f57d07b46eba7}

Deze codesteekproef neemt een gebruikershandvat en krijgt alle het bedrijflidmaatschap van de gebruiker in een serie. De reactie is afgebroken voor de beknoptheid.

**Verzoek**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Antwoord**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
