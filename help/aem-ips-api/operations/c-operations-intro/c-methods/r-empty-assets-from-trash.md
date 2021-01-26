---
description: Legt activa van het IPS afval leeg.
seo-description: Legt activa van het IPS afval leeg.
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Dynamic Media Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Legt activa van het IPS afval leeg.

Activa worden in de prullenbak geplaatst totdat ze handmatig worden geleegd of totdat ze uit de prullenbak stappen. Als ze handmatig worden geleegd, leven ze in de prullenmand tot de volgende opschoontaak (normaal nij) wanneer ze definitief uit het systeem worden verwijderd. Als ze uit de prullenbak stappen, worden de middelen schoongemaakt als onderdeel van dezelfde schoonmaakactie. De time-out kan worden geconfigureerd (de standaardinstellingen zijn 7 dagen).

## Toegestane gebruikerstypen {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parameters {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat eigenaar is van de activa. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | De array van handgrepen die de items vertegenwoordigen die uit de prullenbak moeten worden verwijderd. |

**Output (emptyAssetsFromTrashParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Ja | Het aantal elementen dat met succes uit de prullenbak is verwijderd. |
| `*`warningCount`*` | `xsd:Int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd elementen uit de prullenbak te verwijderen. |
| `*`errorCount`*` | `xsd:Int` | Ja | Het aantal fouten dat is gegenereerd toen de bewerking probeerde elementen uit de prullenbak te verwijderen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde deze uit de prullenbak te verwijderen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde deze uit de prullenbak te verwijderen. |

## Voorbeelden {#section-6154a873b6c342bf92e2036280cafdcf}

In dit codevoorbeeld worden de greep van het bedrijf en een elementgreep-array gebruikt die grepen bevat naar de elementen die uit de prullenbak moeten worden geleegd.

**Verzoek**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Antwoord**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

