---
description: Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.
solution: Experience Manager
title: Kenmerkbestanden van Catalog
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Cataloguskenmerkbestanden{#catalog-attribute-files}

Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.

Cataloguskenmerkbestanden bestaan uit een set tekstrecords, gescheiden door één `<CR>` (ASCII-code `0xD`), één `<LF>` (ASCII-code `0xA`) of een `<CR><LF>`-paar. Elke record bestaat uit een kenmerknaam en een of meer door komma&#39;s gescheiden kenmerkwaarden:

`*``*= *`naamevaluatie`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> waarden</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Kenmerknaam. Kan bestaan uit een of meer letters, cijfers, - en _. Niet hoofdlettergevoelig. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Kenmerkwaarde. Mag geen <span class="codeph"> &lt;CR&gt;</span> of <span class="codeph"> &lt;LF&gt;</span> karakters omvatten, tenzij ontsnapt door één enkele backslash net vóór het newline karakter. </p></td> 
 </tr> 
</table>

Spaties tussen tokens zijn optioneel.

De verslagen met onbekende attributennamen worden genegeerd door de Server van het Platform.

Kenmerknamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot;, &quot;_&quot; en &quot;.&quot;.

Als dezelfde kenmerknaam meerdere keren voorkomt in hetzelfde kenmerkbestand, heeft de laatste aangetroffen naam voorrang.

Gebruik # als het eerste teken om een record te markeren als een opmerking, die de parser negeert.
