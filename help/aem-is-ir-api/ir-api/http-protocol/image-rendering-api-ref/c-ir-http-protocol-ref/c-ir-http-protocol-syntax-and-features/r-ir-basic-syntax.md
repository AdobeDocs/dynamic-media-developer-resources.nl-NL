---
title: Basissyntaxis van HTTP-protocol voor het renderen van afbeeldingen
description: In deze sectie wordt de basissyntaxis beschreven van het Dynamic Media Image Rendering HTTP-protocol.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Basissyntaxis van HTTP-protocol voor het renderen van afbeeldingen{#image-rendering-http-protocol-basic-syntax}

In deze sectie wordt de basissyntaxis beschreven van het Dynamic Media Image Rendering HTTP-protocol.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Item </p> </th> 
   <th colname="col2" class="entry"> <p>Definitie </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> verzoek</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignet</span> ] [?<span class="varname"> modifiers</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> poort</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignet </span> </p> </td> 
   <td colname="col2"> <p>Vignetspecificaties (relatief bestandspad of item voor vignetcatalogus). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifiers </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> opmerking</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>&lbrace; <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Naam van een opdrachtmacro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> opmerking </span> </p> </td> 
   <td colname="col2"> <p>Opmerkingtekenreeks (genegeerd door server). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Naam van een opdracht of kenmerk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Naam van een aangepaste variabele. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>Opdracht of waarde van variabele. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*, en *`var`* zijn niet hoofdlettergevoelig. De server behoudt het hoofdlettergebruik voor alle andere tekenreekswaarden.

**Server-id**

De &#39; `/ir/render`De basiscontext is vereist voor alle HTTP-aanvragen voor het renderen van afbeeldingen.

**Opmerkingen**

Opmerkingen kunnen overal in aanvraagtekenreeksen worden ingesloten en worden geïdentificeerd door een punt (.) onmiddellijk na het opdrachtscheidingsteken (&amp;). De opmerking wordt beëindigd door het volgende exemplaar van een (niet-gecodeerde) opdrachtscheidingsteken. Deze functie kan worden gebruikt om informatie aan het verzoek toe te voegen die niet is bedoeld voor gebruik in de afbeeldingsserver, zoals tijdstempels en database-id&#39;s.

**HTTP-decodering**

Eerst extracten bij het renderen van afbeeldingen *`object`* en *`modifiers`* uit de binnenkomende aanvraag. De *`object`* wordt vervolgens gescheiden in padelementen die afzonderlijk HTTP-gedecodeerd zijn. De *`modifiers`* tekenreeks wordt gescheiden in *`command`*= *`value`* paren, en *`value`* wordt dan HTTP-gedecodeerd vóór bevel-specifieke verwerking.
