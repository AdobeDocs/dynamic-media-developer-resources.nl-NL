---
description: De basissyntaxis van het HTTP-protocol ziet er als volgt uit.
seo-description: De basissyntaxis van het HTTP-protocol ziet er als volgt uit.
seo-title: Basissyntaxis van HTTP-protocol voor afbeeldingen
solution: Experience Manager
title: Basissyntaxis van HTTP-protocol voor afbeeldingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---


# Beeld dat het protocol van HTTP basissyntaxis{#image-serving-http-protocol-basic-syntax} dient

De basissyntaxis van het HTTP-protocol ziet er als volgt uit.

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> verzoek</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modifiers</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_adres</span>[:<span class="varname"> poort</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>Specifier van bronobject (afbeeldingspad of item van afbeeldingscatalogus). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifiers</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> opmerking</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Naam van een opdrachtmacro. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> opmerking</span> </span> </p></td> 
  <td class="stentry"> <p>Opmerkingtekenreeks (genegeerd door server). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Een van de ondersteunde opdrachten- of kenmerknamen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Naam van een aangepaste variabele. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Opdracht of waarde van variabele. </p></td> 
 </tr> 
</table>

*`server_address`*,  *`cmdName`*,  *`macro`* en  *`var`* zijn niet hoofdlettergevoelig. De server behoudt het hoofdlettergebruik voor alle andere tekenreekswaarden.

*`value`* is opdrachtspecifiek en kan bestaan uit een of meer waarden, gescheiden door komma&#39;s. Zie de beschrijving van de afzonderlijke opdrachten voor meer informatie.

## Server-id {#section-926ae55ddba14b8d952147a5fd701e14}

De [!DNL /is/image] wortelcontext wordt vereist voor alle HTTP- verzoeken aan het Serven van het Beeld.

## HTTP-decodering {#section-20922baccd804d2d986b44ce9a183a7d}

Beeldserver extraheert eerst *`object`* en *`modifiers`* uit de binnenkomende aanvraag. *`object`* wordt vervolgens gescheiden in padelementen die afzonderlijk HTTP-gedecodeerd zijn. De *`modifiers`*-tekenreeks wordt gescheiden in *`command`*= *`value`*-paren en *`value`* wordt vervolgens HTTP-gedecodeerd vóór opdrachtspecifieke verwerking.

>[!NOTE]
>
>Tenzij anders vermeld in de documentatie, moeten alle onveilige karakters volgens de norm van HTTP worden gecodeerd. Raadpleeg de HTTP-specificatie voor meer informatie.

## Opmerkingen {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Opmerkingen kunnen overal in aanvraagtekenreeksen worden ingesloten en worden geïdentificeerd door een punt(.) onmiddellijk na het opdrachtscheidingsteken (&amp;). De opmerking wordt beëindigd door het volgende exemplaar van een (niet-gecodeerde) opdrachtscheidingsteken. Deze functie kan worden gebruikt om informatie aan de aanvraag toe te voegen die niet voor gebruik in de afbeeldingsserver is, zoals tijdstempels, database-id&#39;s, enz.

## Zie ook {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Gegevenstypen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa),  [HTTP/1.1-specificatie](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
