---
description: Zoekresultaten met metagegevens die samengevatte informatie over een element bevatten.
seo-description: Zoekresultaten met metagegevens die samengevatte informatie over een element bevatten.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
topic: Scene7 Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 2%

---


# AssetSummary{#assetsummary}

Zoekresultaten met metagegevens die samengevatte informatie over een element bevatten.

Syntaxis

## Parameters {#section-ebc75cc024d94c439260d2e71873cc74}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Asset handle. |
| ` *`type`*` | `xsd:string` | Elementtype. De constante &quot;Elementen&quot;bepaalt de mogelijke waarden. Optioneel. |
| ` *`name`*` | `xsd:string` | Elementnaam. Optioneel. |
| ` *`map`*` | `xsd:string` | De map die het element bevat. |
| ` *`filename`*` | `xsd:string` | Bestandsnaam van element. |
| ` *`gemaakt`*` | `xsd:dateTime` | Aanmaakdatum van element. |
| ` *`createUser`*` | `xsd:string` | De gebruiker die het element heeft gemaakt. |
| ` *`lastModified`*` | `xsd:dateTime` | De datum waarop het element voor het laatst is bijgewerkt. |
| ` *`lastModifyUser`*` | `xsd:string` | De laatste gebruiker die het element heeft gewijzigd. |
| ` *`metadataArray`*` | `types:MetadataArray` | Array met metagegevenswaarden die aan het element zijn gekoppeld. |
| ` *`score`*` | `xsd:double` | Definieert de precisie in het geval van een gelijkenis zoekopdracht (0 = geen overeenkomst, 1 = exacte overeenkomst). |
| ` *`scoreDetail`*` | `xsd:string` | Bevat gedetailleerde informatie over gelijkaardige gebieden als resultaat van een gelijkenis onderzoek. |

