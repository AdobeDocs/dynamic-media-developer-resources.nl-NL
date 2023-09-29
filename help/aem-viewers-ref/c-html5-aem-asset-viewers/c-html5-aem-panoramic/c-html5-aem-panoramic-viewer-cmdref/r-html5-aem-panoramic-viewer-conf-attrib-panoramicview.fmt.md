---
title: PanoramicView.fmt
description: Specificeert het beeldformaat dat door de component voor het laden van beelden van de Server van het Beeld wordt gebruikt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# PanoramicView.fmt{#panoramicview-fmt}

Specificeert het beeldformaat dat door de component voor het laden van beelden van de Server van het Beeld wordt gebruikt. Als de opgegeven indeling eindigt met &quot;-alpha&quot;, worden de afbeeldingen door de component als transparant gerenderd. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een transparante achtergrond. Als u de achtergrondkleur ondoorzichtig wilt maken, stelt u de optie `background-color` CSS-eigenschap naar `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat door de component voor het laden van beelden van de Server van het Beeld moet worden gebruikt. Als de opgegeven indeling eindigt met "-alpha", geeft de component afbeeldingen weer als transparante inhoud; voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een transparante achtergrond. Stel daarom voor dekkend de CSS-eigenschap voor de achtergrondkleur in op de gewenste kleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
