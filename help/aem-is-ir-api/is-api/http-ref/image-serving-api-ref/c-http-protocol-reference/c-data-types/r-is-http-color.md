---
description: Kleurwaarden. U kunt kleurwaarden opgeven met hexadecimale notatie, een door komma's gescheiden lijst met componentwaarden of decimalen.
solution: Experience Manager
title: kleur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 2ff380ad30911a85bc066ae53f0cb69360ed99e4
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 12%

---

# kleur{#color}

Kleurwaarden. U kunt kleurwaarden opgeven met hexadecimale notatie, een door komma&#39;s gescheiden lijst met componentwaarden of decimalen.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> kleur</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&amp;lcub; lcub;<span class="varname"> grijs</span>[,<span class="varname"> alpha</span>][g]&amp;rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> rood</span>,<span class="varname"> groen</span>,<span class="varname"> blauw</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyaan</span>, <span class="varname"> magenta</span>, <span class="varname"> geel</span>, <span class="varname"> zwart</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>_k}&amp;rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rood</span>, <span class="varname"> groen</span>, <span class="varname"> blauw</span>, <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>kleurcomponentwaarde (0...255, decimaal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cyaan</span>, <span class="varname"> magenta</span>, <span class="varname"> geel</span>, <span class="varname"> zwart</span>, <span class="varname"> alpha</span></span> </p></td> 
  <td class="stentry"> <p>Waarde CMYK-kleurcomponent (0..100 %, decimaal int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> grijs</span>, <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>Waarde van grijskleurcomponent (0...100%, decimaal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>gecomprimeerde hexadecimale grijskleurwaarde (GG) van twee cijfers </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>gecomprimeerde hexadecimale grijs met vier cijfers en alpha-kleurwaarde (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>gecomprimeerde zescijferige hexadecimale RGB-kleurwaarde (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>gecomprimeerde hexadecimale RGBA- (RRGGBBAA) of CMYK-kleurwaarde (CCMMYYK) met acht cijfers (indien opgegeven met het achtervoegsel 'k') </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>gecomprimeerde hexadecimale CMYK van tien cijfers met alfawaarde (CCYMMKKAA) </p> </td> 
 </tr> 
</table>

Decimale componentwaarden voor RGB-kleuren liggen in het bereik 0...255. Decimale componentwaarden voor CMYK en grijs liggen in het bereik 0,100%. Alle hexadecimale componentwaarden liggen in het bereik 0...0xFF.

Waarden van kleurcomponenten worden verondersteld onafhankelijk te zijn van de alfawaarde (niet vooraf vermenigvuldigd).

Alle kleurwaarden, voorvoegsels en achtervoegsels zijn niet hoofdlettergevoelig.

Het achtervoegsel &#39;k&#39; is vereist voor CMYK-kleurwaarden. U kunt desgewenst een achtervoegsel voor het type RGB en grijswaarden opgeven.

Het voorvoegsel &#39;0x&#39; is vereist voor hexadecimale grijswaarden.

Met het achtervoegsel &#39;s&#39; wordt opgegeven dat de kleurwaarde is gekoppeld aan de invoer-(bron)kleurruimte die overeenkomt met het pixeltype van de kleurwaarde (gedefinieerd met `attribute::IccProfileSrc*`). Als dit achtervoegsel niet aanwezig is, wordt de kleurwaarde gekoppeld aan de uitvoerkleurruimte (doel) (gedefinieerd met `icc=` of `attribute::IccProfile*`).

## Standaard {#section-737082a7da544acca8092a48d88480e7}

Als een alpha-waarde niet expliciet wordt opgegeven, wordt aangenomen dat deze 255, 0xFF of 100% (volledig dekkend) is.

## Voorbeelden {#section-4ac69026349949f8b595a6d4a9ce474d}

Voorbeelden van geldige kleurspecificaties en het overeenkomende pixeltype, de kleurwaarde, de alfawaarde en de standaardkleurruimte:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>kleur</i> </b> </th> 
   <th class="entry"> <b>Pixeltype</b> </th> 
   <th class="entry"> <b>Kleurwaarde</b> </th> 
   <th class="entry"> <b>Alfa-waarde</b> </th> 
   <th class="entry"> <b>Standaardkleurruimte </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>grijs </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
   <td> <p>grijs </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>grijs </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grijs </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

De uitvoerkleurruimte die is opgegeven met `icc=` wordt toegepast in plaats van de standaardkleurruimte wanneer het pixeltype van een uitvoerkleur overeenkomt met het pixeltype van de uitvoerafbeelding.
