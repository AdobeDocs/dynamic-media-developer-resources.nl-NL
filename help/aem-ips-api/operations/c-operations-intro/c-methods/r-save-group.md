---
description: Maak of bewerk een groep.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# saveGroup{#savegroup}

Maak of bewerk een groep.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep aan het bedrijf met de groep u wilt bewaren. |
| groupHandle | `xsd:string` | Nee | De greep naar de groep. |
| name | `xsd:string` | Ja | Groepsnaam. |
| isSystemDefined | `xsd:boolean` | Ja | `false` is standaard. |

**Output (saveGroupReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| groupHandle | `xsd:string` | Ja | Groepshandgreep. |

## Voorbeelden {#section-26eee227ff1f4edabb7fa1240b4d9999}

Deze codesteekproef leidt tot een groep die tot een specifiek bedrijf behoort. Als de groep al bestaat, wordt deze opgeslagen met de parameterwaarden die u opgeeft.

**Verzoek**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Antwoord**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
