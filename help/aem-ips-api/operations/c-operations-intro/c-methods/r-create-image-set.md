---
description: Hiermee maakt u een afbeeldingsset.
seo-description: Hiermee maakt u een afbeeldingsset.
seo-title: createImageSet
solution: Experience Manager
title: createImageSet
topic: Scene7 Image Production System API
uuid: 688f3954-bc8f-4687-8d66-e064561cd4a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# createImageSet{#createimageset}

Hiermee maakt u een afbeeldingsset.

Syntaxis

## Toegestane gebruikerstypen {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees-/schrijftoegang tot de bestemmingsomslag hebben.

## Parameters {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf waartoe de afbeeldingsset behoort. |
| ` *`folderHandle`*` | `xsd:string` | Ja | De greep naar de map. |
| ` *`name`*` | `xsd:string` | Ja | Naam van afbeeldingsset. |
| ` *`type`*` | `xsd:string` | Ja | Type afbeeldingsset. |
| ` *`thumbAssetHandle`*` | `xsd:string` | Nee | Handgreep van het element dat fungeert als miniatuur voor de nieuwe afbeeldingsset. Als gespecificeerd niet, probeert IPS om het eerste beeldmiddel te gebruiken dat door de reeks van verwijzingen wordt voorzien. |

**Uitvoer**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | De handgreep van de nieuwe afbeeldingsset. |

## Voorbeelden {#section-385fe3b0af8044b0a2451336ec137fc5}

Dit codevoorbeeld leidt tot een beeldreeks die door bedrijf, omslag, naam, en type wordt gespecificeerd. De reactie is een elementgreep van de nieuwe afbeeldingsset.

**Verzoek**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Antwoord**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```

