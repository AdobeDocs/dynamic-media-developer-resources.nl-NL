---
description: Hiermee maakt u een afbeeldingsindeling.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# saveImageFormat{#saveimageformat}

Hiermee maakt u een afbeeldingsindeling.

>[!NOTE]
>
>De `urlModifier` veldwaarde moet bestaan uit geldige XML. Bijvoorbeeld, wijzigen `&` tot `&`. Krijg de `urlModfier` waarde van het IPS gebruikersinterface.

## Geautoriseerde gebruikerstypen {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep naar het bedrijf met de afbeeldingsindeling waarmee u wilt werken. |
| imageFormatHandle | `xsd:string` | Nee | Afbeeldingsformaatgreep die u wilt opslaan. |
| name | `xsd:string` | Ja | Naam afbeeldingsindeling. |
| urlModifier | `xsd:string` | Ja | Dit kan om het even welk IPS koord van de protocolvraag zijn. De gemakkelijkste manier om een bepaling te produceren URL is met het IPS gebruikersinterface tot stand te brengen en dan het vraagkoord te snijden en te kleven. |

**Output (saveImageFormatReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Ja | Verwerk de afbeeldingsindeling. |

## Voorbeelden {#section-c7bd733212ef494297a97093f3af193f}

In dit codevoorbeeld wordt een afbeeldingsindeling gemaakt. In dit voorbeeld: `urlModifier` werd bepaald door zijn waarde in het IPS gebruikersinterface met een geldig formaat van HTML.

**Verzoek**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Antwoord**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
