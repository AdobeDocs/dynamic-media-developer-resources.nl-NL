---
description: Wijzigt de naam van een element.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# renameAsset{#renameasset}

Wijzigt de naam van een element.

>[!NOTE]
>
>De `renameFiles` parameter is vervangen voor eerdere versies en is verwijderd uit `renameAsset`. Het pad van het virtuele bestand wordt gewijzigd en aangepast aan de naam van het nieuwe element (met behoud van de bestandsextensie), maar dit heeft geen invloed op de fysieke bestandspaden. API-clients moeten verwijzingen naar deze parameter verwijderen bij het bijwerken naar de nieuwe API-versie.

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
| companyHandle | `xsd:string` | Ja | De handgreep van de onderneming waartoe het actief behoort. |
| assetHandle | `xsd:string` | Ja | De greep naar het element waarvan u de naam wilt wijzigen. |
| newName | `xsd:string` | Ja | Nieuwe naam van element. |
| validateName | `xsd:boolean` | Ja | Als de `validateName` is `true` en het elementtype vereist een unieke IPS-id, dan wordt de nieuwe naam gecontroleerd op algemene uniciteit en `renameAsset` genereert een fout als deze niet uniek is. |

**Uitvoer (naamAssetReturn wijzigen)**

IPS API keert geen reactie voor deze verrichting terug. Zie de beschrijving van de `<ns1:validateName>` element for caveats about this element.

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
