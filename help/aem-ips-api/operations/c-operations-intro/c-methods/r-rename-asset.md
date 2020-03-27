---
description: Wijzigt de naam van een element.
seo-description: Wijzigt de naam van een element.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameAsset{#renameasset}

Wijzigt de naam van een element.

>[!NOTE]
>
>De `renameFiles` parameter is vervangen voor eerdere versies en verwijderd uit `renameAsset`. Het pad van het virtuele bestand wordt gewijzigd en aangepast aan de naam van het nieuwe element (met behoud van de bestandsextensie), maar dit heeft geen invloed op de fysieke bestandspaden. API-clients moeten verwijzingen naar deze parameter verwijderen bij het bijwerken naar de nieuwe API-versie.

## Geautoriseerde gebruikerstypen {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang tot het element hebben.

## Parameters {#section-ef95a994106841e0ab346dd4cf672258}

**Input (renameAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep van de onderneming waartoe het actief behoort. |
| ` *`assetHandle`*` | `xsd:string` | Ja | De greep naar het element waarvan u de naam wilt wijzigen. |
| ` *`newName`*` | `xsd:string` | Ja | Nieuwe naam van element. |
| ` *`validateName`*` | `xsd:boolean` | Ja | Als `validateName` is `true` en het activatype een unieke IPS identiteitskaart vereist, dan wordt de nieuwe naam gecontroleerd globale uniciteit en `renameAsset` werpt een fout als het niet uniek is. |

**Uitvoer (naamAssetReturn wijzigen)**

IPS API keert geen reactie voor deze verrichting terug. Zie de beschrijving van het `<ns1:validateName>` element voor waarschuwingen over dit element.

## Voorbeelden {#section-a0ddffd62bec42e09069f22ceb486f8a}

In dit codevoorbeeld wordt de naam van een element gewijzigd

**Verzoek**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Antwoord**

Geen.
