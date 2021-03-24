---
description: Hiermee maakt u een nieuw element dat is afgeleid van een bestaand primair bronafbeeldingselement.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# createDerivedAsset{#createderivedasset}

Hiermee maakt u een nieuw element dat is afgeleid van een bestaand primair bronafbeeldingselement.

Syntaxis

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Afgeleide activa specificeren het protocolbevelen van de Server van het Beeld die de vertegenwoordiging van het eigenaarbeeld wijzigen. Met het afgeleide type `AdjustedView` kunt u eenvoudige wijzigingen toepassen op één afbeelding (bijvoorbeeld door een uitsnijdrechthoek op te geven), terwijl de `LayerView` helpt een weergave met meerdere lagen te maken die tekst of extra afbeeldingen kan bevatten.

In tegenstelling tot een afbeeldingskopie (zie [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), wordt een afgeleide afbeelding gekoppeld aan de eigen afbeelding. Door wijzigingen in de afbeelding van de eigenaar worden gekoppelde afgeleide elementen gewijzigd. Als u de afbeelding van de eigenaar verwijdert, worden alle gekoppelde afgeleide afbeeldingen verwijderd.

## Toegestane gebruikerstypen {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-5a0dde01cff6454da3646ea805c2be1e}

**Input (createDerivedAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat het element bevat waaruit u het nieuwe element wilt afleiden. |
| `*`ownerHandle`*` | `xsd:string` | Ja | De handgreep van het primaire afbeeldingselement waaruit de nieuwe afbeelding wordt afgeleid. |
| `*`folderHandle`*` | `xsd:string` | Ja | De handgreep naar de map waarin het nieuwe afgeleide element wordt gemaakt. |
| `*`name`*` | `xsd:string` | Ja | De naam van het afgeleide element. |
| `*`type`*` | `xsd:string` | Ja | Het type actief van het nieuwe afgeleide actief: `AdjustedView` of `LayerView`. |
| `*`urlModifier`*` | `xsd:string` | Nee | Opdrachten van het protocol voor het renderen van afbeeldingen die *voor* de aanvraag of `urlPostApplyModifier` opdrachten zijn toegepast. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nee | Opdrachten van het protocol voor het renderen van afbeeldingen die *after* op de aanvraag of `urlPostApplyModifier`-opdrachten zijn toegepast. |

**Output (createDerivedAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep van het afgeleide element. |

## Voorbeelden {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

De voorbeeldcode maakt een afgeleid element met een aangepaste weergave en `urlModifier` en `urlPostApplyModifier` met willekeurige waarden. De reactie keert de handvat op het onlangs afgeleide activa terug.

**Verzoek**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Antwoord**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```

