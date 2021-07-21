---
description: Hiermee stelt u het groepslidmaatschap voor een gebruiker in.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# setGroupMembership{#setgroupmembership}

Hiermee stelt u het groepslidmaatschap voor een gebruiker in.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nee | De handgreep voor de gebruiker wiens groepslidmaatschap u wilt instellen. |
| `*`companyHandle`*` | `xsd:string` | Nee | Bedrijfshandgreep. |
| `*`groupHandleArray`*` | `types:HandleArray` | Ja | De array van handgrepen naar groepen waartoe de gebruiker behoort. |

**Output (setGroupMembershipReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-67b86d259df24938896fe19061845811}

Deze codesteekproef maakt tot de gebruiker een lid van een groep. Voeg een gebruiker aan veelvoudige groepen met de serie van de groepshandvat toe.

**Verzoek**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Antwoord**

Geen.
