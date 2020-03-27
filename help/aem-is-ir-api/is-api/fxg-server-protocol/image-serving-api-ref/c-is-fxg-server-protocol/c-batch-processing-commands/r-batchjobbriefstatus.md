---
description: Hiermee wordt de samengevatte status van een ingediende taak opgehaald.
seo-description: Hiermee wordt de samengevatte status van een ingediende taak opgehaald.
seo-title: batchjobbriefstatus
solution: Experience Manager
title: batchjobbriefstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobbriefstatus{#batchjobbriefstatus}

Hiermee wordt de samengevatte status van een ingediende taak opgehaald.

Deze parameter:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Taak-id die is verkregen op het moment van verzending. </p> </td> 
 </tr> 
</table>

Retourneert:

Korte status van taak in XML-indeling; fout als de functie ongeldig is of de taak is verwijderd.

## Voorbeeld {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
