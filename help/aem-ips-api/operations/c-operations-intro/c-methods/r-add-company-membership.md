---
description: Hiermee voegt u een gebruiker toe aan een of meer bedrijven.
seo-description: Hiermee voegt u een gebruiker toe aan een of meer bedrijven.
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addCompanyMembership{#addcompanymembership}

Hiermee voegt u een gebruiker toe aan een of meer bedrijven.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Input (addCompanyMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Nee | De handgreep voor de gebruiker wiens lidmaatschap u wilt toevoegen. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Een array van bedrijven waaraan u de gebruiker toevoegt. |

**Output (addCompanyMembershipReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-5469f88bac7047cca131faa6b021e437}

In dit voorbeeld wordt ` *`companyHandleArray`*` gebruikt om een gebruiker aan één bedrijf toe te voegen.

**Verzoek**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Antwoord**

Geen.
