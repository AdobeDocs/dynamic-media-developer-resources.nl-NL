---
description: Haalt de lidmaatschappen van een gebruiker in een bedrijfserie op.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# getCompanyMembership{#getcompanymembership}

Haalt de lidmaatschappen van een gebruiker in een bedrijfserie op.

Syntaxis

## Toegestane gebruikerstypen {#section-f8bba547e1f648648be99dc48fd72b5d}

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
| `*`userHandle`*` | `xsd:string` | Nee | De handgreep aan de gebruiker van wie lidmaatschap u wilt verkrijgen. |

**Output (getCompanyMembershipReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`membershipArray`*` | `types:CompanyMembershipArray` | Ja | Array van lidmaatschap van bedrijven. |

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

