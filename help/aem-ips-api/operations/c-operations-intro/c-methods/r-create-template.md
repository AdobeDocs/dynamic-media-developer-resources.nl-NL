---
description: Hiermee maakt u een gelaagde afbeelding die meerdere tekst- en afbeeldingslagen kan bevatten.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# createTemplate{#createtemplate}

Hiermee maakt u een gelaagde afbeelding die meerdere tekst- en afbeeldingslagen kan bevatten.

De `urlModifier` parameter specificeert de het protocolbevelen van de Server van het Beeld die in de catalogus van de Server van het Beeld worden opgeslagen voorafgaand aan om het even welke user-provided bevelen op URL worden toegepast. De `urlPostApplyModifier` parameter specificeert protocolbevelen worden toegepast na om het even welke bevelen URL, die om het even welke conflicterende gebruiker-geleverde montages met voeten treedt.

## Geautoriseerde gebruikerstypen {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Het bedrijf waartoe de sjabloon behoort. |
| folderHandle | `xsd:string` | Ja | De maphandgreep die staat voor de map waarin de sjabloon zich bevindt. |
| name | `xsd:string` | Ja | Naam sjabloon. |
| type | `xsd:string` | Ja | Sjabloontype. |
| urlModifier | `xsd:string` | Ja | Specificeert de bevelen van de Server van het Beeld die in de catalogus worden opgeslagen IS die voorafgaand aan om het even welke user-provided bevelen op URL worden toegepast. |
| urlPostApplyModifier | `xsd:string` | Nee | Hiermee geeft u protocolopdrachten op die worden toegepast na URL-opdrachten, waarbij conflicterende door de gebruiker opgegeven instellingen worden genegeerd. |

**Uitvoer (createTemplateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | De greep naar de sjabloon. |

## Voorbeelden {#section-09adb4d2f0c944af875c4463a461f55d}

In dit codevoorbeeld wordt een sjabloon gemaakt in een map die is opgegeven door een greep, met een naam van `APIcreateTemplate`, `urlModifier`en `urlPostApplyModifier`. De reactie retourneert de greep naar de nieuwe sjabloon.

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
