---
description: Voegt gebruikers van een specifiek bedrijf aan een specifieke groep toe.
solution: Experience Manager
title: addGroupMember
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# addGroupMember{#addgroupmembers}

Voegt gebruikers van een specifiek bedrijf aan een specifieke groep toe.

Syntaxis

## Toegestane gebruikerstypen {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-b28434dcf2ca4b4ea431136aac33913e}

**Input (addGroupMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| `*`groupHandle`*` | `xsd:string` | Ja | De groepshandgreep. |
| `*`userHandleArray`*` | `types:HandleArray` | Ja | Een array van handgrepen voor gebruikers die u aan een groep wilt toevoegen. |

**Output (addGroupMemberParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-8f168b528aef4c4fa8c3d41f7686842f}

In dit voorbeeld wordt `*`addGroupMemberParam`*` gebruikt om een gebruiker aan één bedrijf toe te voegen. IPS API keert geen reactie voor deze verrichting terug.

**Verzoek**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Antwoord**

Geen.
