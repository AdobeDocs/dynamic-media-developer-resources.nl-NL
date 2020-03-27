---
description: Schaduw- en gloedeffecten in Photoshop-stijl worden geïmplementeerd met behulp van speciale sublagen (effectlagen) die aan elke laag (de bovenliggende laag) kunnen worden gekoppeld, inclusief laag=0 en layer=comp.
seo-description: Schaduw- en gloedeffecten in Photoshop-stijl worden geïmplementeerd met behulp van speciale sublagen (effectlagen) die aan elke laag (de bovenliggende laag) kunnen worden gekoppeld, inclusief laag=0 en layer=comp.
seo-title: Laageffecten
solution: Experience Manager
title: Laageffecten
topic: Scene7 Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Laageffecten{#layer-effects}

Schaduw- en gloedeffecten in Photoshop-stijl worden geïmplementeerd met behulp van speciale sublagen (effectlagen) die aan elke laag (de bovenliggende laag) kunnen worden gekoppeld, inclusief laag=0 en layer=comp.

Effectlagen ondersteunen een aantal standaardkenmerken en -opdrachten voor afbeeldingen en lagen, maar zijn niet bedoeld als algemene lagen en bieden geen ondersteuning voor onafhankelijke afbeeldings- of tekstgegevens.

Een willekeurig aantal laageffecten kan aan één bovenliggende laag worden gekoppeld.

## Binnenste en buitenste effecten {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Binneneffecten* worden boven op de bovenliggende laag weergegeven en zijn alleen zichtbaar in dekkende gebieden van de bovenliggende laag. *Buitenste effecten* worden achter de bovenliggende laag gerenderd (zodat ze nooit zichtbaar zijn binnen dekkende gebieden van de bovenliggende laag) en kunnen op een willekeurige positie in het samengestelde canvas worden geplaatst. Een binnen- of buiteneffect wordt gekozen door een positief of negatief effect laagaantal met het `effect=` bevel toe te wijzen. De `effect=` opdracht bestuurt ook de z-volgorde onder meerdere effectlagen die aan dezelfde bovenliggende laag zijn gekoppeld.

## Verhouding tot bovenliggende laag {#section-eb8bfc4f754a42fc973b562821d6f2d3}

De lagen van het effect worden automatisch gerangschikt en geplaatst om met de ouderlaag (d.w.z. de effect laag erft de `size=` `origin=` en de waarden van de ouderlaag) te samenvallen. `pos=` U kunt de effectlaag ook buiten de bovenliggende laag plaatsen, zoals gewoonlijk is vereist voor slagschaduwen en binnenschaduweffecten. Terwijl voor standaardlagen een verschuiving `pos=` is opgegeven tussen de oorsprong van deze laag en laag 0, `pos=` geeft voor effectlagen de verschuiving aan tussen de oorsprong van de effectlaag en de bovenliggende laag.

## Ondersteunde opdrachten en kenmerken {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Effectlagen accepteren de volgende opdrachten en kenmerken:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Alle andere opdrachten voor afbeeldingen en lagen in effectlagen worden genegeerd.

## Standaardeffectmacro&#39;s {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Om het gebruik van laageffecten te vergemakkelijken, voorziet IS twee macro&#39;s van de standaardafbeeldingscatalogus, `$shadow$` en `$glow$`, die standaardwaarden voor de attributen van de effect laag verstrekken die aan de laageffecten van Photoshop gelijkaardig zijn. De volgende lijst maakt een lijst van welke effect bevel en macro zouden moeten worden gebruikt om de standaardeffecten van de laag uit te voeren. Natuurlijk, kunnen om het even welke die attributen in de macro&#39;s worden gespecificeerd in URL worden gewijzigd, of de alternatieve macro&#39;s kunnen worden gecreeerd om de gevolgen van de douanelaag uit te voeren.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Gewenst effect</b> </th> 
   <th class="entry"> <b> Opdracht</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Slagschaduw </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schaduw binnen </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Gloed buiten </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Gloed binnen </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#section-4c449fdf707b43858917fb271fa1fe96}

Voeg een drie pixels brede, rode rand met een dekking van 50% toe aan een laag:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

De rand volgt de contouren van het alfakanaal of masker van de afbeelding. Als u dit instelt, `effect=1` wordt de rand op de binnenrand geplaatst.

Voeg een schaduw voor een vervaging toe aan een afbeelding met de standaardeffectinstellingen (behalve de kleur):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` Hiermee voegt u een kleine marge toe aan de rechterbenedenranden van de afbeelding, waardoor de slagschaduw niet kan worden bijgesneden tot de afbeeldingsgrenzen.

## Zie ook {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [opdrachtmacro&#39;s%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
