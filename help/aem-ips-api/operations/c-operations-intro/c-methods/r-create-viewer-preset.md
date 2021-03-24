---
description: Hiermee maakt u een voorinstellingsweergave die bepaalt wat een gebruiker kan zien. De kijker kan van om het even welk type beschikbaar in IPS zijn. De voorinstellingsweergave wordt toegepast wanneer de elementen worden gepubliceerd.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer-voorinstellingen
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# createViewerPreset{#createviewerpreset}

Hiermee maakt u een voorinstellingsweergave die bepaalt wat een gebruiker kan zien. De kijker kan van om het even welk type beschikbaar in IPS zijn. De voorinstellingsweergave wordt toegepast wanneer de elementen worden gepubliceerd.

Syntaxis

## Toegestane gebruikerstypen {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Input (createViewerPresetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf dat de voorinstellingen en elementen van de viewer bevat. |
| `*`folderHandle`*` | `xsd:string` | Ja | De greep van de map die de elementen bevat. |
| `*`name`*` | `xsd:string` | Ja | Naam van viewer. |
| `*`type`*` | `xsd:string` | Ja | Type viewer. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Nee | Een array met namen, waarden en grepen van afbeeldingen waarop u voorinstellingen toepast. |

**Uitvoer (createViewerPresetReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Ja | Verwerk de voorinstelling aan de viewer. |

## Voorbeelden {#section-c88ea63536f3461cbe4677ba53f875dd}

In dit codevoorbeeld wordt een voorinstelling voor een videospeler gemaakt. Het antwoord retourneert een greep naar de voorinstelling.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Antwoord**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```

