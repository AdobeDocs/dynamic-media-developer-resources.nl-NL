---
description: Updates publiceren contextstatus voor een element.
seo-description: Updates publiceren contextstatus voor een element.
seo-title: ContextStateUpdate
solution: Experience Manager
title: ContextStateUpdate
topic: Dynamic Media Image Production System API
uuid: ef579d3c-1899-4088-903e-e6ed5a414ca8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# ContextStateUpdate{#contextstateupdate}

Updates publiceren contextstatus voor een element.

Syntaxis

## Parameters {#section-9f747df071854c6896fdbb95684ad947}

Stel de publicatiecontextstatus van een element in met `setAssetsContextState`.

<table id="table_FD172CEA4EFE44E08ADA22D090DC06CA">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Naam </th>
   <th colname="col2" class="entry"> Type </th>
   <th colname="col3" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:tekenreeks </span></td>
   <td colname="col3"> Verwerk de publicatiecontext. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:tekenreeks</span></td>
   <td colname="col3">De bijgewerkte gepubliceerde status van het element voor de opgegeven publicatiecontext. Omvat: 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> MarkedForPublish</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarkedForPublish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [Status publiceren](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)

