---
description: Hiermee wordt de gedetailleerde status van een ingediende taak opgehaald.
seo-description: Hiermee wordt de gedetailleerde status van een ingediende taak opgehaald.
seo-title: batchjobdetailedstatus
solution: Experience Manager
title: batchjobdetailedstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdetailedstatus{#batchjobdetailedstatus}

Hiermee wordt de gedetailleerde status van een ingediende taak opgehaald.

Deze parameter:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Taak-id die is verkregen op het moment van verzending. </p> </td> 
 </tr> 
</table>

Retourneert:

Gedetailleerde status van taak in XML-indeling; fout als `jobid` ongeldig is of taak is verwijderd.

## Voorbeeld {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
