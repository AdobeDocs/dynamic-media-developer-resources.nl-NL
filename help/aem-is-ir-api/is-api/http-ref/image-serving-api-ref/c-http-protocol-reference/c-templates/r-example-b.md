---
description: Vergelijkbare vereisten als Voorbeeld A, maar gebruik een achtergrond met een effen kleur en laat de hoogte van de samenstelling variëren, om afbeeldingen met verschillende hoogte-breedteverhoudingen te kunnen gebruiken.
seo-description: Vergelijkbare vereisten als Voorbeeld A, maar gebruik een achtergrond met een effen kleur en laat de hoogte van de samenstelling variëren, om afbeeldingen met verschillende hoogte-breedteverhoudingen te kunnen gebruiken.
seo-title: Voorbeeld B
solution: Experience Manager
title: Voorbeeld B
topic: Scene7 Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

De afbeelding wordt in laag 0 geplaatst en de hoogtewaarde van `size=` is ingesteld op 0. Hierdoor wordt de werkelijke hoogte bepaald door de hoogte van de afbeelding nadat deze is geschaald naar 800 pixels breed.

`extend=` Hiermee voegt u 100 pixels boven en onder en 200 pixels rechts toe.

De oorsprong voor zowel laag 0 als laag 1 wordt midden-rechts van het compositiegebied geplaatst om de gewenste tekstpositie te bereiken.

In de volgende afbeelding ziet u het samengestelde resultaat voor verschillende hoogte-breedteverhoudingen van de afbeelding en verschillende tekstreeksen.

![](assets/exampleb.png)

