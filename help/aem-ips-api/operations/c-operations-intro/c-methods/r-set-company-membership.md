---
description: Hiermee stelt u het lidmaatschap van een gebruiker in een of meer bedrijven in.
seo-description: Hiermee stelt u het lidmaatschap van een gebruiker in een of meer bedrijven in.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Scene7 Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanyMembership{#setcompanymembership}

Hiermee stelt u het lidmaatschap van een gebruiker in een of meer bedrijven in.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-3930dc6a016140178631083563598104}

**Input (setCompanyMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:sting` | Nee | Gebruikershandgreep. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Serie van bedrijven. |

**Output (setCompanyMembershipParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-862c0cc32ce0407ab248028e690a8386}

Deze codesteekproef voegt een gebruiker aan een bedrijf toe. Geef indien nodig meerdere bedrijven in de handle array op.

**Verzoek**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Antwoord**

Geen.
