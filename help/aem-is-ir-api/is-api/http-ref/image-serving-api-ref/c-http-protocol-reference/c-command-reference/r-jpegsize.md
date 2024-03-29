---
title: jpegSize
description: JPEG-grootte in kiloBytes. Hiermee geeft u de maximale grootte van de JPEG-respons op in kilobytes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# jpegSize{#jpegsize}

JPEG-grootte in kiloBytes. Hiermee geeft u de maximale grootte van de JPEG-respons op in kilobytes.

`jpegSize= *`size`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p> </td> 
  <td class="stentry"> <p>Grootte in kilobytes. </p></td> 
 </tr> 
</table>

Als deze waarde is ingesteld op een positieve waarde en als de JPEG-respons met de opgegeven JPEG-kwaliteit deze waarde niet overschrijdt, wordt die afbeelding geretourneerd als reactie. Anders neemt de kwaliteit van de JPEG af totdat een afbeelding wordt gemaakt die past in de opgegeven grootte of totdat wordt bepaald dat de afbeelding niet past. In het laatste geval ontbreekt het verzoek met een fout.

De waarde 0 betekent dat de respons niet wordt beperkt door de grootte.

Negatieve waarden zijn niet toegestaan.

## Eigenschappen {#section-19e544e77d35478b98fe8666f27d6968}

Request-kenmerk. Ongeacht de huidige laaginstelling. Genegeerd als de indeling van de uitvoerafbeelding niet JPEG is.

## Standaard {#section-198b798ed187453197e0969c641d6fb5}

0

## Voorbeeld {#section-46bf806fd3ef4875b7726df32b6f834d}

De garantiegrootte is niet te groot voor levering aan een apparaat met beperkt geheugen:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Zie ook {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [kenmerk:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
