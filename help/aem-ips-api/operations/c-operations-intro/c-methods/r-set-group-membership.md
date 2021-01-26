---
description: Hiermee stelt u het groepslidmaatschap voor een gebruiker in.
seo-description: Hiermee stelt u het groepslidmaatschap voor een gebruiker in.
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
topic: Dynamic Media Image Production System API
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# setGroupMembership{#setgroupmembership}

Hiermee stelt u het groepslidmaatschap voor een gebruiker in.

Syntaxis

## Toegestane gebruikerstypen {#section-3d6308a8a5694ed085e04d1c37982b9e}

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
