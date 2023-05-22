---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`getal`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Optimalisatie inschakelen, beperken of uitschakelen voor apparaten waarbij <span class="codeph"> devicePixelRatio</span> is groter dan <span class="codeph"> 1</span>, dat wil zeggen apparaten met een hoge dichtheid zoals iPhone4 en soortgelijke apparaten. Als de component actief is, beperkt de component de grootte van de aanvraag voor de IS-afbeelding alsof het apparaat alleen een pixelverhouding van <span class="codeph"> 1</span> en dus de bandbreedte verminderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> getal</span></span> </p> </td> 
   <td colname="col2"> <p> Als u de <span class="codeph"> limiet</span> Met deze instelling schakelt u een hoge pixeldichtheid alleen in tot de opgegeven limiet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
