---
description: Opdrachtwaarden moeten http-gecodeerd zijn met gebruik van %xx escape-reeksen, zodat de waardetekenreeksen de gereserveerde tekens '=', '&' en '%' niet bevatten.
seo-description: Opdrachtwaarden moeten http-gecodeerd zijn met gebruik van %xx escape-reeksen, zodat de waardetekenreeksen de gereserveerde tekens '=', '&' en '%' niet bevatten.
seo-title: HTTP-codering van afbeeldingsserver
solution: Experience Manager
title: HTTP-codering van afbeeldingsserver
topic: Scene7 Image Serving - Image Rendering API
uuid: e7fb368b-060a-439e-95a1-16b94d4796dc
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 19%

---


# Beeld dat HTTP-codering{#image-serving-http-encoding} rendert

Opdrachtwaarden moeten http-gecodeerd zijn met gebruik van %xx escape-reeksen, zodat de waardetekenreeksen de gereserveerde tekens &#39;=&#39;, &#39;&amp;&#39; en &#39;%&#39; niet bevatten.

Anders zijn de standaard HTTP-coderingsregels van toepassing. De HTTP-specificatie vereist codering van de onveilige tekens en van eventuele besturingstekens, zoals `<return>` en `<tab>`. De URL-codering van een teken bestaat uit een symbool &quot;%&quot;, gevolgd door de hexadecimale representatie (hoofdlettergevoelig) van twee cijfers van het ISO-Latijnse codepunt voor het teken. De onveilige tekens en codepunten zijn:

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Onveilig teken </th> 
   <th colname="col2" class="entry"> Codepunten (hex) </th> 
   <th colname="col3" class="entry"> Codepunten (dec) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Spatie </p> </td> 
   <td colname="col2"> <p>20 </p> </td> 
   <td colname="col3"> <p>32 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lt;&gt; </p> </td> 
   <td colname="col2"> <p>3C </p> </td> 
   <td colname="col3"> <p>60 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&gt; </p> </td> 
   <td colname="col2"> <p>3E </p> </td> 
   <td colname="col3"> <p>62 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>" </p> </td> 
   <td colname="col2"> <p>22 </p> </td> 
   <td colname="col3"> <p>34 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aantal </p> </td> 
   <td colname="col2"> <p>23 </p> </td> 
   <td colname="col3"> <p>35 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>25 </p> </td> 
   <td colname="col3"> <p>37 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;accolade; </p> </td> 
   <td colname="col2"> <p>7 ter </p> </td> 
   <td colname="col3"> <p>123 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;trace; </p> </td> 
   <td colname="col2"> <p>7D </p> </td> 
   <td colname="col3"> <p>125 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>| </p> </td> 
   <td colname="col2"> <p>7 C </p> </td> 
   <td colname="col3"> <p>124 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>\ </p> </td> 
   <td colname="col2"> <p>5C </p> </td> 
   <td colname="col3"> <p>92 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>^ </p> </td> 
   <td colname="col2"> <p>5E </p> </td> 
   <td colname="col3"> <p>94 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~ </p> </td> 
   <td colname="col2"> <p>7 E </p> </td> 
   <td colname="col3"> <p>126 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbrack; </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrack; </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>` </p> </td> 
   <td colname="col2"> <p>60 </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

Gereserveerde tekens moeten ook worden gecodeerd.

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gereserveerd teken </th> 
   <th colname="col2" class="entry"> Codepunten (Hex) </th> 
   <th colname="col3" class="entry"> Codepunten (dec) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>$ </p> </td> 
   <td colname="col2"> <p>24 </p> </td> 
   <td colname="col3"> <p>36 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp; </p> </td> 
   <td colname="col2"> <p>26 </p> </td> 
   <td colname="col3"> <p>38 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+ </p> </td> 
   <td colname="col2"> <p>2B </p> </td> 
   <td colname="col3"> <p>43 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>, </p> </td> 
   <td colname="col2"> <p>2C </p> </td> 
   <td colname="col3"> <p>44 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>/ </p> </td> 
   <td colname="col2"> <p>2F </p> </td> 
   <td colname="col3"> <p>47 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>: </p> </td> 
   <td colname="col2"> <p>3 bis. </p> </td> 
   <td colname="col3"> <p>58 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>; </p> </td> 
   <td colname="col2"> <p>3B </p> </td> 
   <td colname="col3"> <p>59 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>= </p> </td> 
   <td colname="col2"> <p>3D </p> </td> 
   <td colname="col3"> <p>61 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? </p> </td> 
   <td colname="col2"> <p>3F </p> </td> 
   <td colname="col3"> <p>63 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>@ </p> </td> 
   <td colname="col2"> <p>40 </p> </td> 
   <td colname="col3"> <p>64 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-b85895e5b6a84b96b7fca987656dd34d}

`…&$text=rate&weight=85% 27#&…`

Als er geen verduistering wordt toegepast, moet het bovenstaande aanvraagfragment als volgt worden gecodeerd:

`…&$text=rate%26weight%3D85%25%2027%23&…`

Als er verduistering is toegepast, kan de codering worden beperkt tot het verwijderen van &#39;=&#39;, &#39;&amp;&#39; en &#39;%&#39; tekens:

`…&$text=rate%26weight%3D85%25 27#&…`

## Zie ook {#section-295476ec34c74973962d07dfa9eb2180}

[Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [HTTP/1.1 Specification (RFC 2616)](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
