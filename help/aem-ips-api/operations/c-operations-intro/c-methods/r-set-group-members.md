---
description: Hiermee stelt u het groepslidmaatschap in van gebruikers die tot een specifiek bedrijf behoren.
solution: Experience Manager
title: setGroupMember
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# setGroupMember{#setgroupmembers}

Hiermee stelt u het groepslidmaatschap in van gebruikers die tot een specifiek bedrijf behoren.

De bewerking genereert een verificatiefout als u geen rechten hebt om deze bewerking uit te voeren. Dit is ook waar als om het even welke gebruikers in de gebruikershandvatserie niet tot het bedrijf behoren dat in het bedrijfshandvat wordt gespecificeerd,

## Toegestane gebruikerstypen {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`groupHandle`*` | `xsd:string` | Ja | Groepshandgreep. |
| `*`userHandleArray`*` | `types:HandleArray` | Ja | Array met handgrepen voor gebruikers van wie u het groepslidmaatschap wilt instellen. |

**Output (setGroupMembesReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-9c528c3f44a141ce9eaddf634f26c487}

In dit codevoorbeeld wordt groepslidmaatschap voor één gebruiker ingesteld.

**Verzoek**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Antwoord**

Geen.
