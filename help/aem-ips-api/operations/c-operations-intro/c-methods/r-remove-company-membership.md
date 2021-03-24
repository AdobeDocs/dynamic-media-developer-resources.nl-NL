---
description: Hiermee verwijdert u een gebruiker uit een of meer bedrijven.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# removeCompanyMembership{#removecompanymembership}

Hiermee verwijdert u een gebruiker uit een of meer bedrijven.

Syntaxis

## Toegestane gebruikerstypen {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Input (removeCompanyMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nee | De handgreep voor de gebruiker met het lidmaatschap dat u wilt verwijderen. |
| `*`companyHandleArray`*` | `types:HandleArray` | Ja | De handgreep van het bedrijf waarvan u de gebruiker verwijdert. |

**Output (removeCompanyMembershipReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-6b7903195e8647a1bd0502f87387ca62}

Deze codesteekproef verwijdert een gebruiker uit een bedrijf. Laat de facultatieve gebruikersgreep weg om alle gebruikers uit de bedrijven te verwijderen die in de bedrijfshandvatserie worden gespecificeerd.

**Verzoek**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Antwoord**

Geen.
