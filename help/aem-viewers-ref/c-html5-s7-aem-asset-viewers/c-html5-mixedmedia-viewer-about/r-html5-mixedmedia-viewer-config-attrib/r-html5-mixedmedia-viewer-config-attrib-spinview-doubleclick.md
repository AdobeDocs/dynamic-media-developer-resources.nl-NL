---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van dubbelklikken/tikken om handelingen te draaien. Instellen op <span class="codeph"> none </span> Schakelt dubbelklikken/tikken om te draaien uit. Indien ingesteld op <span class="codeph"> zoomen </span>, door in één centrifugestap op de afbeelding te klikken; Met CTRL en klikken draait u één centrifuge uit. Instellen op <span class="codeph"> reset </span> zorgt ervoor dat met één klik op de afbeelding de centrifuge wordt teruggezet op het oorspronkelijke centrifugeniveau. Voor <span class="codeph"> zoomReset </span>wordt opnieuw ingesteld als de huidige centrifugefactor gelijk is aan of groter is dan de opgegeven limiet, anders wordt de centrifuge toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` op bureaubladcomputers; `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
