---
description: Maak of bewerk een groep.
seo-description: Maak of bewerk een groep.
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
topic: Scene7 Image Production System API
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---


# saveGroup{#savegroup}

Maak of bewerk een groep.

Syntaxis

## Toegestane gebruikerstypen {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de groep u wilt bewaren. |
| ` *`groupHandle`*` | `xsd:string` | Nee | De greep naar de groep. |
| ` *`name`*` | `xsd:string` | Ja | Groepsnaam. |
| ` *`isSystemDefined`*` | `xsd:boolean` | Ja | `false` is standaard. |

**Output (saveGroupReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | Ja | Groepshandgreep. |

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

