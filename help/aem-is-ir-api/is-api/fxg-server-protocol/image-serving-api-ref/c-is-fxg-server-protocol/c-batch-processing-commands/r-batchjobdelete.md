---
description: Verwijder de uitvoer van een taak.
seo-description: Verwijder de uitvoer van een taak.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# batchjobdelete{#batchjobdelete}

Verwijder de uitvoer van een taak.

Als een taak momenteel wordt uitgevoerd, wordt deze onmiddellijk gestopt en worden alle verwerkingsgegevens verwijderd. Als de taak met succes is voltooid, wordt het uitvoerbestand verwijderd.

Deze parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Taak-id die is verkregen op het moment van verzending. </p></td> 
 </tr> 
</table>

Retourneert:

Status van taak op het moment dat het verwijderingsverzoek werd ontvangen, fout als `jobid` ongeldig is of de taak al was verwijderd.

## Voorbeeld {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
