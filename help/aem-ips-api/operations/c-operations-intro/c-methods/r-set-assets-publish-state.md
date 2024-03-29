---
description: Hiermee wordt bepaald of een reeks elementen gereed is om te worden gepubliceerd.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# setAssetsPublishState{#setassetspublishstate}

Hiermee wordt bepaald of een reeks elementen gereed is om te worden gepubliceerd.

Dit is de batchversie van [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Geautoriseerde gebruikerstypen {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang tot het element hebben.

## Parameters {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Bedrijfshandgreep. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Ja | Array met publicatiestatus voor de elementen. |

**Output (setAssetsPublishStateParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Het aantal correct bijgewerkte elementen. |
| warningCount | `xsd:int` | Ja | Het aantal elementen dat een waarschuwing heeft gegenereerd toen de bewerking probeerde deze bij te werken. |
| errorCount | `xsd:int` | Ja | Het aantal elementen dat een fout heeft gegenereerd toen de bewerking probeerde deze te verwijderen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nee | Details verbonden aan de activa updates die een waarschuwing produceerden. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nee | Details verbonden aan de activa updates die een fout produceerden. |

## Voorbeelden {#section-38cfdd3436214a06a1bae16875501d51}

In dit codevoorbeeld wordt de publicatiestatus van een element ingesteld.

**Verzoek**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Antwoord**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```
