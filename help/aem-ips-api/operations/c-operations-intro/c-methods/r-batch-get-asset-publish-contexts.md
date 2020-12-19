---
description: Retourneert de publicatiecontext voor elementen die zijn gemarkeerd voor publicatie.
seo-description: Retourneert de publicatiecontext voor elementen die zijn gemarkeerd voor publicatie.
seo-title: batchGetAssetPublishContext
solution: Experience Manager
title: batchGetAssetPublishContext
topic: Scene7 Image Production System API
uuid: 7f442019-37a9-4473-be92-a952a7a67664
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# batchGetAssetPublishContext{#batchgetassetpublishcontexts}

Retourneert de publicatiecontext voor elementen die zijn gemarkeerd voor publicatie.

Syntaxis

## Toegestane gebruikerstypen {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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
>* De gebruiker moet lees toegang hebben om de activa terug te keren.
>* Alle gebruikers hebben toegang tot het gedeelde bedrijf.

>



## Parameters {#section-1742fcb196224545b270eb8241f757a8}

**Input (batchGetAssetPublishContextParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| ` *`assetHandleArray`*` | ` `types:HandleArray&quot; | Ja | Een lijst met elementen die u wilt opvragen voor actieve (gemarkeerde voor publicatie) contexten. |

**Output (batchGetAssetPublishContextReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetPublishContextArray`*` | `types:assetPublishContextsArray` | Ja | Een array van publicatiecontexten waarin elk element is gemarkeerd voor publicatie. |

## Voorbeelden {#section-457f6809ccfa425b9a0976313d613f4e}

**Verzoek**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Antwoord**

```java
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```

