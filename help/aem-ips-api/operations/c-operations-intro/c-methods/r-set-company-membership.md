---
description: Hiermee stelt u het lidmaatschap van een gebruiker in een of meer bedrijven in.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

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
| userHandle | `xsd:sting` | Nee | Gebruikershandgreep. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Serie van bedrijven. |

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
