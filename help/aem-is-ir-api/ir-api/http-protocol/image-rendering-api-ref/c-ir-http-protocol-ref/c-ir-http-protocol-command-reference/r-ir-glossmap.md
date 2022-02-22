---
title: glossmap
description: Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# glossmap {#glossmap}

Afbeelding met glans. Biedt pixelcontrole over de glanzen van een herhaalbare structuur, achtergrond/rand of decal.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;Accolade;'is&amp;lbrace;'<span class="varname"> isReq</span>&amp;Broce;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;resource;' </span> </p></td> 
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

Van toepassing op materialen zoals metaalverfeffecten, afgesneden folieachtergronden en -randen, en metaaldraad.

De glanzende-kaartafbeelding moet 8-bits grijswaarden hebben en dezelfde grootte hebben als de primaire afbeelding die u met `src=`. Zie de beschrijving van [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) voor aanvullende informatie.

## Eigenschappen {#section-26375672d69849be9b026cc93c3bc558}

Materiaalkenmerk. Ondersteund door herhaalbare structuren, achtergronden en randen, en cijfers. Genegeerd door materiaal met effen kleuren, kabinetten en vensterbekleding. Zie [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) voor aanvullende informatie.

## Standaard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Geen.

## Zie ook {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
