---
description: Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.
solution: Experience Manager
title: Kenmerkbestanden van Catalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Kenmerkbestanden van Catalog{#catalog-attribute-files}

Kenmerkbestanden van catalogus kunnen elke naam hebben, maar moeten het achtervoegsel .ini hebben. U kunt ze eenvoudig onderhouden met elke teksteditor.

Kenmerkbestanden van catalogus bestaan uit een set tekstrecords, gescheiden door één bestand `<CR>` (ASCII-code) `0xD`), één `<LF>` (ASCII-code) `0xA`), of een `<CR><LF>` paar. Elke record bestaat uit een kenmerknaam en een of meer door komma&#39;s gescheiden kenmerkwaarden:

`*`name`*= *`waarden`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> waarden</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> waarden</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Kenmerknaam. Kan bestaan uit een of meer letters, cijfers, - en _. Niet hoofdlettergevoelig. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Kenmerkwaarde. Mag niet omvatten <span class="codeph"> &lt;cr&gt;</span> of <span class="codeph"> &lt;lf&gt;</span> tekens, tenzij deze worden beschermd door één backslash vlak voor het nieuwe-regelteken. </p></td> 
 </tr> 
</table>

Spaties tussen tokens zijn optioneel.

Records met onbekende kenmerknamen worden door de [!DNL Platform Server].

Kenmerknamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot;, &quot;_&quot; en &quot;.&quot;.

Als dezelfde kenmerknaam meerdere keren voorkomt in hetzelfde kenmerkbestand, heeft de laatste aangetroffen naam voorrang.

Gebruik # als het eerste teken om een record te markeren als een opmerking, die de parser negeert.
