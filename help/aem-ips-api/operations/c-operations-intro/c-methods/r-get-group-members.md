---
description: Haalt de gebruikers op die tot een specifiek bedrijf en een specifieke groep behoren.
seo-description: Haalt de gebruikers op die tot een specifiek bedrijf en een specifieke groep behoren.
seo-title: getGroupMember
solution: Experience Manager
title: getGroupMember
topic: Dynamic Media Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# getGroupMember{#getgroupmembers}

Haalt de gebruikers op die tot een specifiek bedrijf en een specifieke groep behoren.

Syntaxis

## Toegestane gebruikerstypen {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-b798b06354c946abbb90fa72cc9c67fd}

**Input (getGroupMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| `*`groupHandle`*` | `xsd:string` |  | De greep naar de groep. |

**Output (getGroupMemberReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Ja | Een array met gebruikershandgrepen. |

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

