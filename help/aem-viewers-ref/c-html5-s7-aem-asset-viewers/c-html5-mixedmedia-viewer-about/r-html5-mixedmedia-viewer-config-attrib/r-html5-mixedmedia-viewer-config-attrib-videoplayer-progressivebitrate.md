---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 94de31cd-2b4e-4247-b181-26666767f065
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Geeft (in kBit per seconde of kbps) de gewenste videobitsnelheid op voor afspelen vanuit een adaptieve videoset als het huidige systeem geen ondersteuning biedt voor adaptieve videoweergave. </p> <p>De component pakt de videostream op met de dichtstbijzijnde (maar niet meer dan) bitsnelheid voor de opgegeven waarde. Als alle videostreams in de Adaptive Video Set een hogere kwaliteit hebben dan de opgegeven waarde, kiest de logica de bitsnelheid met de laagste kwaliteit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
