---
description: Vergelijkbare vereisten als Voorbeeld A, maar gebruik een achtergrond met een effen kleur en laat de hoogte van de samenstelling variëren, om afbeeldingen met verschillende hoogte-breedteverhoudingen te kunnen gebruiken.
solution: Experience Manager
title: Voorbeeld B
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Voorbeeld B{#example-b}

Vergelijkbare vereisten als Voorbeeld A, maar gebruik een achtergrond met een effen kleur en laat de hoogte van de samenstelling variëren, om afbeeldingen met verschillende hoogte-breedteverhoudingen te kunnen gebruiken.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalogus::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalogus::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$..rtf-encoding&amp;rotate=-90&amp;origin N=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

De afbeelding wordt in laag 0 geplaatst en de hoogtewaarde `size=` wordt ingesteld op 0, waardoor de werkelijke hoogte wordt bepaald door de hoogte van de afbeelding nadat deze is geschaald naar 800 pixels breed.

`extend=` Hiermee voegt u 100 pixels boven en onder en 200 pixels rechts toe.

De oorsprong voor zowel laag 0 als laag 1 wordt midden-rechts van het compositiegebied geplaatst om de gewenste tekstpositie te bereiken.

In de volgende afbeelding ziet u het samengestelde resultaat voor verschillende hoogte-breedteverhoudingen van de afbeelding en verschillende tekstreeksen.

![](assets/exampleb.png)
