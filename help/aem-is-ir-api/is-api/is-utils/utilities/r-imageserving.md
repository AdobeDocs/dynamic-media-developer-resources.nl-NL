---
description: Beeldserver, besturingsscript. Dit manuscript wordt gebruikt om, het Beeld te beginnen tegen te houden of, de Supervisor van de Server van het Beeld opnieuw te beginnen, die beurtelings begint, houdt tegen, of begint alle andere Beeld Servend componenten opnieuw.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# ImageServing{#imageserving}

Beeldserver, besturingsscript. Dit manuscript wordt gebruikt om, het Beeld te beginnen tegen te houden of, de Supervisor van de Server van het Beeld opnieuw te beginnen, die beurtelings begint, houdt tegen, of begint alle andere Beeld Servend componenten opnieuw.

## Gebruik {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## Opdrachten {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opdracht </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> start </span> </p> </td> 
   <td colname="col2"> <p> Begin de Supervisor van de Server en al ander Beeld Servend componenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stoppen </span> </p> </td> 
   <td colname="col2"> <p> Stop al Beeld Servend componenten, met inbegrip van de Supervisor van de Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opnieuw opstarten </span> </p> </td> 
   <td colname="col2"> <p>Begin alle Beeld Serend componenten, met inbegrip van de Supervisor van de Server opnieuw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> starten, { ps | is | svg } </span> </p> </td> 
   <td colname="col2"> <p> Start Tomcat/[!DNL Platform Server], de Afbeeldingsserver, of SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Retourneert uptime en actuele informatie over geheugengebruik voor de Image Server, Tomcat/[!DNL Platform Server], en SVGserver, of status voor slechts de gespecificeerde server; een informatiebericht in plaats daarvan is teruggekeerd als de Supervisor van de Server niet loopt. </p> </td> 
  </tr> 
 </tbody> 
</table>
