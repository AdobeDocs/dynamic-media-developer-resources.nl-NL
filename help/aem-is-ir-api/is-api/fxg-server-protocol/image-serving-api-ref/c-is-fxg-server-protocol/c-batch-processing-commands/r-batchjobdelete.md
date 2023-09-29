---
title: batchjobdelete
description: Verwijder de uitvoer van een taak.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# batchjobdelete{#batchjobdelete}

Verwijder de uitvoer van een taak.

Als een taak momenteel wordt uitgevoerd, wordt deze onmiddellijk gestopt en worden alle verwerkingsgegevens verwijderd. Als de taak met succes is voltooid, wordt het uitvoerbestand verwijderd.

Deze parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>Taak-id die is verkregen op het moment van verzending. </p></td> 
 </tr> 
</table>

Retourneert:

Status van de taak op het moment dat de aanvraag voor verwijdering is ontvangen, fout als `jobid` is ongeldig of de taak is al verwijderd.

## Voorbeeld {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
