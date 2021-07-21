---
description: Hiermee verwijdert u een groep.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# deleteGroup{#deletegroup}

Hiermee verwijdert u een groep.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-42775102ec724c36ae5241eea1a00b8e}

**Input (deleteGroupParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf dat tot de groep behoort die u wilt verwijderen. |
| `*`groupHandle`*` | `xsd:string` | Ja | De handgreep van de groep die u wilt verwijderen. |

**Output (deleteGroupParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Met deze voorbeeldcode wordt een groep uit een bedrijf verwijderd. Hiervoor is een groepshandgreep vereist, die u uit een andere bewerking moet ophalen.

**Verzoek**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Antwoord**

Geen.
