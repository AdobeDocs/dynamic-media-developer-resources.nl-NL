---
title: Kenmerkbestanden van Catalog
description: Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Kenmerkbestanden van Catalog{#catalog-attribute-files}

Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten een `.ini` achtervoegsel bestand. U kunt ze eenvoudig onderhouden met elke teksteditor.

Kenmerkbestanden van catalogus bestaan uit een set tekstrecords, gescheiden door één bestand `<CR>` (ASCII-code 0xD), één `<LF>` (ASCII-code 0xA), of een `<CR><LF>` paar. Elke record bestaat uit een kenmerknaam en een of meer door komma&#39;s gescheiden kenmerkwaarden:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Kenmerknaam; kan bestaan uit een of meer letters, cijfers, - (afbreekstreepje) en _ (onderstrepingsteken); niet hoofdlettergevoelig.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Kenmerkwaarde; mag geen waarde bevatten <span class="codeph"> &lt;cr&gt; </span>, of <span class="codeph"> &lt;lf&gt; </span> tekens, tenzij deze worden beschermd door één backslash vlak voor het nieuwe-regelteken. </p> </td> 
 </tr> 
</table>

* Spaties tussen tokens zijn optioneel.
* De [!DNL Platform Server] Hiermee worden records met onbekende kenmerknamen genegeerd.
* Kenmerknamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en `-`, `_`, en `.` tekens.
* Als dezelfde kenmerknaam meerdere keren voorkomt in hetzelfde kenmerkbestand, heeft de laatste aangetroffen naam voorrang.
* Gebruiken `#` als het eerste teken om een record te markeren als een opmerking die de parser negeert.
