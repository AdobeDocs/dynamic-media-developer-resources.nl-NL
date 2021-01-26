---
description: Hiermee voegt u een gebruiker toe aan een of meer bedrijven.
solution: Experience Manager
title: addCompanyMembership
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# addCompanyMembership{#addcompanymembership}

Hiermee voegt u een gebruiker toe aan een of meer bedrijven.

Syntaxis

## Toegestane gebruikerstypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Input (addCompanyMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nee | De handgreep voor de gebruiker wiens lidmaatschap u wilt toevoegen. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Een array van bedrijven waaraan u de gebruiker toevoegt. |

**Output (addCompanyMembershipReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-5469f88bac7047cca131faa6b021e437}

In dit voorbeeld wordt `*`companyHandleArray`*` gebruikt om een gebruiker aan één bedrijf toe te voegen.

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
