---
title: Kenmerkbestanden van Catalog
description: Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Kenmerkbestanden van Catalog{#catalog-attribute-files}

Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten een `.ini` achtervoegsel bestand. U kunt ze eenvoudig onderhouden met elke teksteditor.

Kenmerkbestanden van catalogus bestaan uit een set tekstrecords, gescheiden door één bestand `<CR>` (ASCII-code 0xD), één `<LF>` (ASCII-code 0xA), of een `<CR><LF>` paar. Elke record bestaat uit een kenmerknaam en een of meer door komma&#39;s gescheiden kenmerkwaarden:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Kenmerknaam; kan bestaan uit een of meer letters, cijfers, '-' en '_'; niet hoofdlettergevoelig. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Kenmerkwaarde; mag geen waarde bevatten <span class="codeph"> &lt;cr&gt; </span>, of <span class="codeph"> &lt;lf&gt; </span> tekens, tenzij deze worden beschermd door één backslash vlak voor het nieuwe-regelteken. </p> </td> 
 </tr> 
</table>

* Spaties tussen tokens zijn optioneel.
* Records met onbekende kenmerknamen worden genegeerd door de [!DNL Platform Server].
* Kenmerknamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot;, &quot;_&quot; en &quot;.&quot;
* Als dezelfde kenmerknaam meerdere keren voorkomt in hetzelfde kenmerkbestand, heeft de laatste aangetroffen naam voorrang.
* Gebruik &#39;#&#39; als het eerste teken om een record te markeren als een opmerking die de parser negeert.
