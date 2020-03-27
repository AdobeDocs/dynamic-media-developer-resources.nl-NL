---
description: Hiermee verwijdert u een groep.
seo-description: Hiermee verwijdert u een groep.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Scene7 Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf dat tot de groep behoort die u wilt verwijderen. |
| ` *`groupHandle`*` | `xsd:string` | Ja | De handgreep van de groep die u wilt verwijderen. |

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
