---
description: Hiermee verwijdert u bedrijfgebruikers uit een specifieke groep.
solution: Experience Manager
title: removeGroupMember
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# removeGroupMember{#removegroupmembers}

Hiermee verwijdert u bedrijfgebruikers uit een specifieke groep.

**Verschillen tussen verwijderopdrachten**

* `removeGroupMembers`: Hiermee verwijdert u meerdere gebruikers uit een groep.
* `removeGroupMembership`: Verwijdert een individuele gebruiker uit een serie van groepen.

## Toegestane gebruikerstypen {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de gebruikers u wilt werken met. |
| `*`groupHandle`*` | `xsd:string` | Ja | Groepshandgreep. |
| `*`userHandleArray`*` | `types:HandleArray` | Ja | Een array van handgrepen voor gebruikers van wie u het groepslidmaatschap wilt verwijderen. |

**Output (removeGroupMemberParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-9eedac852cea46ec80de6a6928bf97ac}

Deze codesteekproef verwijdert een gebruiker uit het gespecificeerde bedrijf. Verwijder meerdere gebruikers uit een groep met de gebruikershandle-array.

**Verzoek**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Antwoord**

Geen.
