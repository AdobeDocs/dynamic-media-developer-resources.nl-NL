---
description: Geeft een array van alle bedrijven.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# getAllCompanies{#getallcompanies}

Geeft een array van alle bedrijven.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parameters {#section-efd74992e6904ebabe7383b577af4fdb}

**Input (getAllCompaniesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| includeExpired | `xsd:boolean` | Ja | Stel dit in op true om verlopen en niet-verlopen bedrijven te retourneren. |

**Output (getAllCompaniesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyArray | `types:CompanyArray` | Ja | De array van bedrijven. |

## Voorbeelden {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Deze codesteekproef keert alle bedrijven in IPS in een serie terug. Let op: de reactie van het monster wordt afgebroken voor de beknoptheid.

**Verzoek**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**Antwoord**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```
