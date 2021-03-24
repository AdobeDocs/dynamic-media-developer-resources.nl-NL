---
description: Hiermee worden gebruikers verwijderd uit een array van groepen.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# removeGroupMembership{#removegroupmembership}

Hiermee worden gebruikers verwijderd uit een array van groepen.

**Verschillen tussen verwijderopdrachten**

* `removeGroupMembers`: Hiermee verwijdert u meerdere gebruikers uit een groep.
* `removeGroupMembership`: Verwijdert een individuele gebruiker uit een serie van groepen.

## Toegestane gebruikerstypen {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input (removeGroupMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nee | De handgreep aan het bedrijf waarvan groepslidmaatschap u wilt verwijderen. |
| `*`groupHandleArray`*` | `types:HandleArray` | Ja | De serie van handvatten aan groepen waarvan u het bedrijf wilt worden verwijderd. |

**Output (removeGroupMembershipReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-f8d4181170a243efb9faf5824ae96197}

Dit codevoorbeeld verwijdert een gebruiker uit een groep.

**Verzoek**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Antwoord**

Geen.
