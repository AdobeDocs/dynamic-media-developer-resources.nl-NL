---
description: Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.
seo-description: Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.
seo-title: Kenmerkbestanden van Catalog
solution: Experience Manager
title: Kenmerkbestanden van Catalog
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# Cataloguskenmerkbestanden{#catalog-attribute-files}

Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.

Cataloguskenmerkbestanden bestaan uit een set tekstrecords, gescheiden door één `<CR>` (ASCII-code 0xD), één `<LF>` (ASCII-code 0xA) of een `<CR><LF>`-paar. Elke record bestaat uit een kenmerknaam en een of meer door komma&#39;s gescheiden kenmerkwaarden:

` *``*= *``*&#42;[, *`naamevaluatiewaarde`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Kenmerknaam; mag bestaan uit een of meer letters, cijfers, '-' en '_'; niet hoofdlettergevoelig. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Kenmerkwaarde; <span class="codeph"> &lt;CR&gt; </span>, of <span class="codeph"> &lt;LF&gt; </span> karakters niet omvatten, tenzij beschermd door één enkele backslash net vóór het newline karakter. </p> </td> 
 </tr> 
</table>

* Spaties tussen tokens zijn optioneel.
* De verslagen met onbekende attributennamen worden genegeerd door de Server van het Platform.
* Kenmerknamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot;, &quot;_&quot; en &quot;.&quot;
* Als dezelfde kenmerknaam meerdere keren voorkomt in hetzelfde kenmerkbestand, heeft de laatste aangetroffen naam voorrang.
* Gebruik &#39;#&#39; als het eerste teken om een record te markeren als een opmerking die de parser negeert.

