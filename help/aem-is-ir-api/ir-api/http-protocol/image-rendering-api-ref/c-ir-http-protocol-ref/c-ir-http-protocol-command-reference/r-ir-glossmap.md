---
description: Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.
seo-description: Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.
seo-title: glossmap
solution: Experience Manager
title: glossmap
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# glossmap{#glossmap}

Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;Markeren;Markeren;'is&amp;Marce;'<span class="varname"> isReq</span>'&amp;brace;'&amp;trace;|&amp;Marce;'&amp;Marce;'&amp;Marce;'<span class="varname"> foreignReq</span>'&amp;Rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Afbeeldingsbestand met glansafbeelding (grijswaarden). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Verzoek aan de Server van het Beeld. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Verzoek aan een externe server. </p></td> 
 </tr> 
</table>

Van toepassing op materialen zoals metaalverfeffecten, afgesneden folieachtergronden en -randen, metaaldraad en dergelijke.

De glanzende-kaartafbeelding moet 8-bits grijswaarden hebben en precies dezelfde grootte hebben als de primaire afbeelding die met `src=`is opgegeven. Zie de beschrijving van [ voor `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) meer informatie.

## Eigenschappen {#section-26375672d69849be9b026cc93c3bc558}

Materiaalkenmerk. Ondersteund door herhaalbare structuren, achtergronden en randen, en cijfers. Genegeerd door materiaal met effen kleuren, kabinetten en vensterbekleding. Zie [ voor meer informatie `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Standaard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Geen.

## Zie ook {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
