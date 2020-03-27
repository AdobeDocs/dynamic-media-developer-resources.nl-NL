---
description: Verwijdert een project van een bedrijf. De verbindingen tussen de activa en het project zijn gebroken, maar de activa worden niet geschrapt van IPS.
seo-description: Verwijdert een project van een bedrijf. De verbindingen tussen de activa en het project zijn gebroken, maar de activa worden niet geschrapt van IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Scene7 Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteProject{#deleteproject}

Verwijdert een project van een bedrijf. De verbindingen tussen de activa en het project zijn gebroken, maar de activa worden niet geschrapt van IPS.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Input (deleteProjectParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | De naam van het bedrijf dat aan het project is gekoppeld. |
| ` *`projectHandle`*` | `xsd:string` | Ja | De handgreep van het te verwijderen project. |

**Output (deleteProjectReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-e38507f1f7ec41b9a625f47390490254}

Deze codesteekproef gebruikt het bedrijfshandvat en het projecthandvat als gebieden in deleteProjectParam die naar de IPS de dienstenserver van het Web wordt verzonden om het project te schrappen.

**Verzoek**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Antwoord**

Geen.
