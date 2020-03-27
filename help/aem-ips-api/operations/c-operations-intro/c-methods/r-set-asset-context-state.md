---
description: Stel de publicatiestatus voor een of meer elementen in of werk deze bij. U kunt afzonderlijke publicatiestatussen instellen voor elke publicatiecontext in een bedrijf.
seo-description: Stel de publicatiestatus voor een of meer elementen in of werk deze bij. U kunt afzonderlijke publicatiestatussen instellen voor elke publicatiecontext in een bedrijf.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Scene7 Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsContextState{#setassetscontextstate}

Stel de publicatiestatus voor een of meer elementen in of werk deze bij. U kunt afzonderlijke publicatiestatussen instellen voor elke publicatiecontext in een bedrijf.

## Geautoriseerde gebruikerstypen {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees toegang hebben om de activa terug te keren.

## Parameters {#section-009b9006de8e4c16ad657c47f28ace9f}

**Input (setAssetsContextStateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| ` *`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | Ja | Een array met elementen en de bijbehorende nieuwe publicatiestatus. |

**Output (setAssetsContextStateReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Het aantal elementen is gewijzigd. |
| ` *`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd elementen te wijzigen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat is gegenereerd toen de bewerking probeerde elementen te wijzigen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | Array met fouten die door elementen worden gegenereerd wanneer de bewerking probeerde deze te wijzigen. |

## Voorbeelden {#section-283a073f3cb14bcda5abed863c538aa4}

In dit codevoorbeeld wordt de publicatiestatus van een element ingesteld met `NotMarkedForPublish`.

**Verzoek**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Antwoord**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

