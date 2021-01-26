---
description: Markeringen toepassen. Geeft aanvullende renderopties aan.
seo-description: Markeringen toepassen. Geeft aanvullende renderopties aan.
seo-title: vlaggen
solution: Experience Manager
title: vlaggen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# flags{#flags}

Markeringen toepassen. Geeft aanvullende renderopties aan.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Vlagwaarde. </p></td> 
 </tr> 
</table>

Wordt momenteel alleen gebruikt voor materiaal in kabinetten.

`flags=0` (standaardinstelling) geeft de bovenste kasten weer met effen deuren.

`flags=1` Hiermee worden de bovenste kasten met glazen deuren weergegeven (als het vignet met glazen deuren was ontworpen).

## Eigenschappen {#section-a2b00d7bb15e449ea85178acb92d8285}

Materiaalkenmerk. Wordt genegeerd als er geen materiaal in de behuizing is of als het object in de doelbehuizing geen glazen deuren toestaat.

## Standaard {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` voor geen glazen deuren.
