---
description: Beeldserver, besturingsscript. Dit manuscript wordt gebruikt om, het Beeld te beginnen tegen te houden of, de Supervisor van de Server van het Beeld opnieuw te beginnen, die beurtelings begint, houdt tegen, of begint alle andere Beeld Servend componenten opnieuw.
seo-description: Beeldserver, besturingsscript. Dit manuscript wordt gebruikt om, het Beeld te beginnen tegen te houden of, de Supervisor van de Server van het Beeld opnieuw te beginnen, die beurtelings begint, houdt tegen, of begint alle andere Beeld Servend componenten opnieuw.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <p> <span class="codeph"> starten, { ps| is| svg } </span> </p> </td> 
   <td colname="col2"> <p> Start Tomcat/Platform Server, de Image Server of SVG opnieuw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps| is| svg ] </span> </p> </td> 
   <td colname="col2"> <p>Keert uptime en huidige informatie van het geheugengebruik voor de Server van het Beeld, de Server van Tomcat/van het Platform, en de server SVG, of status voor enkel de gespecificeerde server terug; een informatiebericht in plaats daarvan is teruggekeerd als de Supervisor van de Server niet loopt. </p> </td> 
  </tr> 
 </tbody> 
</table>

