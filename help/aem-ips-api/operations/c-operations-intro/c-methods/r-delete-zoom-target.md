---
description: Hiermee verwijdert u een zoomdoel.
seo-description: Hiermee verwijdert u een zoomdoel.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
topic: Scene7 Image Production System API
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteZoomTarget{#deletezoomtarget}

Hiermee verwijdert u een zoomdoel.

## Geautoriseerde gebruikerstypen {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang tot het element hebben.

## Parameters {#section-225330a45e7a408f8375e084677d9cb1}

**Input (deleteZoomTargetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf waartoe het zoomdoel behoort. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Ja | De handgreep van het zoomdoel dat moet worden verwijderd. |

**Output (deleteZoomTargetParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeeld {#section-a35857a5ca884357a879f7ba6cf985fe}

In dit codevoorbeeld wordt een zoomdoel van een bedrijf verwijderd.

**Verzoek**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Antwoord**

Geen.
