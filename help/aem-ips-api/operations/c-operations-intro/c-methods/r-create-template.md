---
description: Hiermee maakt u een gelaagde afbeelding die meerdere tekst- en afbeeldingslagen kan bevatten.
seo-description: Hiermee maakt u een gelaagde afbeelding die meerdere tekst- en afbeeldingslagen kan bevatten.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Scene7 Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# createTemplate{#createtemplate}

Hiermee maakt u een gelaagde afbeelding die meerdere tekst- en afbeeldingslagen kan bevatten.

De `urlModifier` parameter specificeert de het protocolbevelen van de Server van het Beeld in de catalogus van de Server van het Beeld die voorafgaand aan om het even welke user-provided bevelen op URL worden toegepast. Met de parameter `urlPostApplyModifier` worden protocolopdrachten opgegeven die worden toegepast na URL-opdrachten. Deze overschrijven eventuele conflicterende door de gebruiker opgegeven instellingen.

## Toegestane gebruikerstypen {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Het bedrijf waartoe de sjabloon behoort. |
| ` *`folderHandle`*` | `xsd:string` | Ja | De maphandgreep die staat voor de map waarin de sjabloon zich bevindt. |
| ` *`name`*` | `xsd:string` | Ja | Sjabloonnaam. |
| ` *`type`*` | `xsd:string` | Ja | Sjabloontype. |
| ` *`urlModifier`*` | `xsd:string` | Ja | Specificeert de bevelen van de Server van het Beeld die in de catalogus worden opgeslagen IS die voorafgaand aan om het even welke user-provided bevelen op URL worden toegepast. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Nee | Hiermee geeft u protocolopdrachten op die worden toegepast na URL-opdrachten. Deze overschrijven eventuele conflicterende door de gebruiker opgegeven instellingen. |

**Uitvoer (createTemplateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | De greep naar de sjabloon. |

## Voorbeelden {#section-09adb4d2f0c944af875c4463a461f55d}

In dit codevoorbeeld wordt een sjabloon gemaakt in een map die door een greep wordt opgegeven, met de naam `APIcreateTemplate`, a `urlModifier` en a `urlPostApplyModifier`. De reactie retourneert de greep naar de nieuwe sjabloon.

**Verzoek**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Antwoord**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```

