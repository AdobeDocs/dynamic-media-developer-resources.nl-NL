---
description: Haalt de gebruikers op die tot een specifiek bedrijf en een specifieke groep behoren.
solution: Experience Manager
title: getGroupMember
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# getGroupMember{#getgroupmembers}

Haalt de gebruikers op die tot een specifiek bedrijf en een specifieke groep behoren.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-b798b06354c946abbb90fa72cc9c67fd}

**Input (getGroupMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| groupHandle | `xsd:string` |  | De greep naar de groep. |

**Output (getGroupMemberReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | Ja | Een array met gebruikershandgrepen. |

## Voorbeelden {#section-aaa340dba6b64cce9bcd8303cf999166}

Deze codesteekproef keert een gebruikershandvatserie terug die alle gebruikers bevat die tot een specifieke groep behoren.

**Verzoek**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Antwoord**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
