---
description: Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.
solution: Experience Manager
title: glossmap
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# glossmap{#glossmap}

Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;Broce;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Verzoek aan een externe server. </p></td> 
 </tr> 
</table>

Van toepassing op materialen zoals metaalverfeffecten, afgesneden folieachtergronden en -randen, metaaldraad en dergelijke.

De glanzende kaartafbeelding moet 8-bits grijswaarden hebben en precies dezelfde grootte hebben als de primaire afbeelding die met `src=` is opgegeven. Raadpleeg de beschrijving van [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) voor meer informatie.

## Eigenschappen {#section-26375672d69849be9b026cc93c3bc558}

Materiaalkenmerk. Ondersteund door herhaalbare structuren, achtergronden en randen, en cijfers. Genegeerd door materiaal met effen kleuren, kabinetten en vensterbekleding. Zie [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) voor aanvullende informatie.

## Standaard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Geen.

## Zie ook {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
