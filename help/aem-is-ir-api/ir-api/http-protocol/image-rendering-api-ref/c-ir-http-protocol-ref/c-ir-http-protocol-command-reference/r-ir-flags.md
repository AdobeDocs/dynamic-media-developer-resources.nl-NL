---
title: vlaggen
description: Markeringen toepassen. Geeft aanvullende renderopties aan.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# vlaggen {#flags}

Markeringen toepassen. Geeft aanvullende renderopties aan.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Vlagwaarde. </p></td> 
 </tr> 
</table>

Wordt momenteel alleen gebruikt voor materiaal in kabinetten.

`flags=0` (Standaard) Hiermee maakt u bovenste kasten met effen deuren.

`flags=1` Hiermee worden de bovenste kasten met glazen deuren gerenderd (als het vignet met glazen deuren is ontworpen).

## Eigenschappen {#section-a2b00d7bb15e449ea85178acb92d8285}

Materiaalkenmerk. Wordt genegeerd als er geen materiaal in de behuizing is of als het object in de doelbehuizing geen glazen deuren toestaat.

## Standaard {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Voor geen glazen deuren.
