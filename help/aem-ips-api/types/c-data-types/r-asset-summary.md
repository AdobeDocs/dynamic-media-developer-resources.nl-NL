---
title: AssetSummary
description: Zoekresultaten met metagegevens die samengevatte informatie over een element bevatten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# [!DNL AssetSummary]{#assetsummary}

Zoekresultaten met metagegevens die samengevatte informatie over een element bevatten.

Syntaxis

## Parameters {#section-ebc75cc024d94c439260d2e71873cc74}

| Naam | Type | Beschrijving |
|---|---|---|
| assetHandle | `xsd:string` | Asset handle. |
| type | `xsd:string` | Elementtype. De constante &quot;Elementen&quot;bepaalt de mogelijke waarden. Optioneel. |
| name | `xsd:string` | Elementnaam. Optioneel. |
| map | `xsd:string` | De map die het element bevat. |
| filename | `xsd:string` | Bestandsnaam van element. |
| gemaakt | `xsd:dateTime` | Aanmaakdatum van element. |
| createUser | `xsd:string` | De gebruiker die het element heeft gemaakt. |
| lastModified | `xsd:dateTime` | De datum waarop het element voor het laatst is bijgewerkt. |
| lastModifyUser | `xsd:string` | De laatste gebruiker die het element heeft gewijzigd. |
| metadataArray | `types:MetadataArray` | Een array met metagegevenswaarden die aan het element zijn gekoppeld. |
| score | `xsd:double` | Definieert de precisie als er een gelijkenis zoekopdracht is (0 = geen overeenkomst, 1 = exacte overeenkomst). |
| scoreDetail | `xsd:string` | Het bevat gedetailleerde informatie over gelijkaardige gebieden als resultaat van een gelijkenis onderzoek. |
