---
description: textPs= steunt een aantal verschillende gebruiksmodellen die in deze sectie worden beschreven.
seo-description: textPs= steunt een aantal verschillende gebruiksmodellen die in deze sectie worden beschreven.
seo-title: Tekstlagen
solution: Experience Manager
title: Tekstlagen
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---


# Tekstlagen{#text-layers}

textPs= steunt een aantal verschillende gebruiksmodellen die in deze sectie worden beschreven.

>[!NOTE]
>
>Deze sectie is niet van toepassing op `text=`.

De gemeenschappelijke regels en definities zijn als volgt:

* Tekstlagen waarvan het formaat automatisch wordt aangepast, zijn lagen die geen `size=` opdracht bevatten of waarvoor `size=0,0` is opgegeven.

* De laaggrootte van tekstlagen die zichzelf aanpassen, wordt bepaald door de werkelijke weergegeven tekst.
* Het standaardlaaganker van tekstlagen die zichzelf aanpassen bevindt zich gewoonlijk *niet* in het midden van de laag (zie hieronder).
* Als `anchor=` of `origin=` wordt gespecificeerd voor het zelf-rangschikken van tekstlagen, wordt de positie van de tekstlaag beïnvloed door de tekstinhoud.

* Wanneer `size=` is opgegeven, kunnen delen van tekenglyphs buiten de laagrechthoek worden weergegeven.
* `pos=` U kunt de positie van een tekstlaag altijd wijzigen.

## Punttekst (zelfaanpassing) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punttekst in Photoshop-stijl wordt gesimuleerd wanneer deze `textPs=` is opgegeven zonder `size=`, `textPath=`of `textFlowPath=`. De laaggrootte wordt horizontaal bepaald door de breedte van de gerenderde tekst en verticaal door de regelafstand. Tekst loopt nooit automatisch om.

Als noch `anchor=` noch `origin=` gespecificeerd is, wordt de eerste lijn van de tekst geplaatst direct boven de laagoorsprong; alinea&#39;s die met `\ql` een markering zijn gemarkeerd, worden rechts van de oorsprong van de laag geplaatst, alinea&#39;s die met de alinea&#39;s beginnen, `\qr` worden links van de oorsprong gerenderd en alinea&#39;s die met de alinea&#39;s zijn gemarkeerd, `\qc` worden horizontaal om de oorsprong gecentreerd. De standaardregels voor laagpositionering zijn van toepassing als `anchor=` of `origin=` .

Als `color=` wordt opgegeven, wordt het selectiekader van de werkelijke tekst gevuld.

De volgende RTF-opdrachten worden genegeerd: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rechthoekig tekstvak {#section-1d3ab11df26d4004a1a801546756475d}

Als `size=` wordt opgegeven naast `textPs=` (zonder `textPath=` en `textFlowPath=`), wordt de tekst beperkt tot de opgegeven rechthoek. De laag wordt op de gebruikelijke wijze gepositioneerd. Tekenglyphs bij de randen van het tekstvak kunnen gedeeltelijk buiten het tekstvak worden weergegeven.

`color=` vult het gebied dat wordt gedefinieerd door `size=`.

Alle RTF-opdrachten worden toegepast zoals verwacht.

## Tekstvak voor variabele hoogte {#section-e1233d1c9f8e43218667361dc0c4fd06}

Wanneer u `size=` met 0 hoogte opgeeft, kan het formaat van het tekstvak verticaal worden aangepast aan alle inhoud. De laagbreedte wordt gedefinieerd door de breedte van `size=`en de laaghoogte door de hoogte van de werkelijke weergegeven tekst. De laag wordt op de gebruikelijke wijze gepositioneerd. Tekenglyphs bij de linker- en rechterrand van het tekstvak kunnen gedeeltelijk buiten het tekstvak worden weergegeven.

`color=` Hiermee vult u de rechthoek die wordt gedefinieerd door de opgegeven breedte `size=` en de hoogte van de werkelijke tekst.

De volgende RTF-opdrachten worden genegeerd:

`\vertal*`

## Tekst in pad automatisch vergroten/verkleinen {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` samen met `textPs=` kan worden gebruikt om een of meer gebieden te definiëren waarin tekst moet worden doorlopen. `textFlowXPath=` kan optioneel worden opgegeven om te voorkomen dat tekst in een of meer gebieden doorloopt. Als `size=` deze optie niet is opgegeven, wordt de resulterende tekstlaag zichzelf in grootte aangepast en wordt de laaggrootte bepaald door het selectiekader van de daadwerkelijk weergegeven tekst.

Als er geen `origin=` `anchor=` of geen laaganker is opgegeven, krijgt het laaganker standaard (0,0) van de pixelcoördinaatruimte die wordt gebruikt om het pad of de paden te definiëren, zodat absolute positionering wordt gegarandeerd, ongeacht de weergegeven tekst. Wanneer `anchor=` of `origin=` wordt opgegeven, wordt de laag ten opzichte van (en aangepast aan) het selectiekader van de daadwerkelijk gerenderde inhoud geplaatst.

`color=` Hiermee vult u het selectiekader van de werkelijke tekst die wordt weergegeven.

De volgende RTF-opdrachten worden genegeerd:

`\marg*`

## Tekst van vooraf formaat in pad {#section-ed492a8a54414cd4bde360500cec6968}

Als `size=` deze samen met `textFlowPath=`de laaggrootte is opgegeven, wordt de laaggrootte vooraf bepaald. (0,0) van de pixelcoördinaatruimte die wordt gebruikt om het pad of de paden te definiëren, bevindt zich in de linkerbovenhoek van de laagrechthoek.

De `textFlowPath=` gebieden kunnen zich buiten de laagrechthoek bevinden. Tekst wordt altijd in alle padgebieden laten doorlopen en gerenderd, zelfs als dit ertoe leidt dat tekst buiten de laagrechthoek wordt gerenderd. `extend=0,0,0,0`U kunt de gerenderde tekst uitsnijden naar de laagrechthoek.

Voor laagpositioneringsdoeleinden is de laagrechthoek gebaseerd op de opgegeven waarde, `size=`ongeacht hoeveel tekst wordt weergegeven, zelfs als een gedeelte zich buiten de laagrechthoek bevindt. Standaardlaagpositionering is van toepassing.

`color=` Hiermee vult u het rechthoekige gebied dat wordt gedefinieerd door `size=`.

De volgende RTF-opdrachten worden genegeerd voor `textFlowPath=`:

`\marg*`

## Tekst op pad automatisch vergroten/verkleinen {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definieert een of meer paden waarop de tekst die met is opgegeven, `textPs=` moet worden gerenderd. Wanneer `size=` geen waarde is opgegeven, wordt de grootte van de resulterende tekstlaag automatisch aangepast. De laaggrootte wordt bepaald door het selectiekader van de werkelijke tekst die wordt gerenderd.

Als er geen `origin=` of geen waarde `anchor=` is opgegeven, is het laaganker standaard ingesteld op (0,0) van de pixelcoördinaatruimte die wordt gebruikt om het pad te definiëren; de positie van de gerenderde tekst is vast, ongeacht hoeveel tekst wordt gerenderd. Wanneer `anchor=` of `origin=` wordt opgegeven, wordt de laag ten opzichte van (en aangepast aan) het selectiekader van de daadwerkelijk gerenderde inhoud geplaatst.

`color=` Hiermee vult u het selectiekader van de werkelijke tekst die wordt weergegeven.

De volgende RTF-opdrachten worden genegeerd:

* `\marg*`
* `\hyph*`
* `\vertal*`

Alle tekst na de eerste `\par` of `\line` wordt genegeerd.

## Tekst van vooraf formaat op pad {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Als `size=` deze samen met `textPath=`de laaggrootte is opgegeven, wordt de laaggrootte vooraf bepaald. (0,0) van de pixelcoördinaatruimte die wordt gebruikt om het pad of de paden te definiëren, bevindt zich in de linkerbovenhoek van de laagrechthoek.

De paden kunnen zich geheel of gedeeltelijk buiten de laagrechthoek bevinden. Tekst wordt altijd toegepast en gerenderd langs het gehele pad, zelfs buiten de laagrechthoek. `extend=0,0,0,0` U kunt de gerenderde tekst uitsnijden naar de laagrechthoek.

Voor laagpositioneringsdoeleinden is de laagrechthoek gebaseerd op het opgegeven `size=`, zelfs als een deel van de tekst buiten de laagrechthoek wordt weergegeven. Standaardlaagpositionering is van toepassing.

`color=` vult het gebied dat door wordt bepaald `size=`.

De volgende RTF-opdrachten worden genegeerd:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Alle tekst na de eerste `\par` of `\line` wordt genegeerd.
