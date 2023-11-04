---
description: textPs= steunt een aantal verschillende gebruiksmodellen die in deze sectie worden beschreven.
solution: Experience Manager
title: Tekstlagen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Tekstlagen{#text-layers}

textPs= steunt een aantal verschillende gebruiksmodellen die in deze sectie worden beschreven.

>[!NOTE]
>
>Deze sectie is niet van toepassing op `text=`.

De gemeenschappelijke regels en definities zijn als volgt:

* Tekstlagen waarvan het formaat automatisch wordt aangepast, zijn lagen die geen a `size=` bevel of waarvoor `size=0,0` wordt opgegeven.

* De laaggrootte van tekstlagen die zichzelf aanpassen, wordt bepaald door de werkelijke weergegeven tekst.
* Het standaardlaaganker van tekstlagen waarvan het formaat automatisch wordt aangepast is doorgaans *niet* in het midden van de laag (zie hieronder).
* Indien `anchor=` of `origin=` is opgegeven voor het automatisch aanpassen van tekstlagen, wordt de positie van de tekstlaag beïnvloed door de tekstinhoud.

* Wanneer `size=` worden opgegeven, kunnen delen van tekenglyphs buiten de laagrechthoek worden weergegeven.
* `pos=` U kunt de positie van een tekstlaag altijd wijzigen.

## Punttekst (automatisch aanpassen aan grootte) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punttekst in Photoshop-stijl wordt gesimuleerd wanneer `textPs=` is opgegeven zonder `size=`, `textPath=`, of `textFlowPath=`. De laaggrootte wordt horizontaal bepaald door de breedte van de gerenderde tekst en verticaal door de regelafstand. Tekst loopt nooit automatisch door.

Als geen van beide `anchor=` noch `origin=` worden opgegeven, wordt de eerste regel van de tekst direct boven de oorsprong van de laag geplaatst; alinea&#39;s die zijn gemarkeerd met `\ql` worden rechts van de oorsprong van de laag geplaatst, alinea&#39;s die `\qr` worden links van de oorsprong weergegeven, en alinea&#39;s met `\qc` horizontaal om de oorsprong zijn gecentreerd. De standaardregels voor laagpositionering zijn van toepassing als `anchor=` of `origin=` worden opgegeven.

Indien `color=` wordt opgegeven, wordt het selectiekader van de werkelijke tekst gevuld.

De volgende RTF-opdrachten worden genegeerd: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rechthoekig tekstvak {#section-1d3ab11df26d4004a1a801546756475d}

Indien `size=` wordt gespecificeerd naast `textPs=` (zonder `textPath=` en `textFlowPath=`), wordt tekst beperkt tot de opgegeven rechthoek. De laag wordt op de gebruikelijke wijze gepositioneerd. Tekenglyphs bij de randen van het tekstvak kunnen gedeeltelijk buiten het tekstvak worden weergegeven.

`color=` vult het gebied dat is gedefinieerd door `size=`.

Alle RTF-opdrachten worden toegepast zoals u had verwacht.

## Tekstvak voor variabele hoogte {#section-e1233d1c9f8e43218667361dc0c4fd06}

Opgeven `size=` met een hoogte van 0, kan het formaat van het tekstvak verticaal worden aangepast aan alle inhoud. De laagbreedte wordt gedefinieerd door de breedte van `size=`en de laaghoogte met de hoogte van de werkelijk gerenderde tekst. De laag wordt op de gebruikelijke wijze gepositioneerd. Tekenglyphs bij de linker- en rechterrand van het tekstvak kunnen gedeeltelijk buiten het tekstvak worden weergegeven.

`color=` vult de rechthoek die wordt gedefinieerd door de breedte die is opgegeven met `size=` en de hoogte van de werkelijke weergegeven tekst.

De volgende RTF-opdrachten worden genegeerd:

`\vertal*`

## Tekst in pad automatisch vergroten/verkleinen {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in combinatie met `textPs=` kan worden gebruikt om een of meer gebieden te definiëren waarin tekst moet worden doorlopen. `textFlowXPath=` kan optioneel worden opgegeven om te voorkomen dat tekst in een of meer gebieden doorloopt. Indien `size=` niet wordt opgegeven, heeft de resulterende tekstlaag een eigen grootte en wordt de laaggrootte bepaald door het selectiekader van de daadwerkelijk weergegeven tekst.

Als geen van beide `origin=` noch `anchor=` opgegeven, wordt voor het laaganker standaard (0,0) van de pixelcoördinaatruimte gebruikt om het pad of de paden te definiëren, zodat absolute positionering wordt gegarandeerd, ongeacht de weergegeven tekst. Indien `anchor=` of `origin=` worden opgegeven, wordt de laag ten opzichte van (en aangepast aan) het selectiekader van de daadwerkelijk gerenderde inhoud geplaatst.

`color=` Hiermee vult u het selectiekader van de werkelijke tekst die wordt weergegeven.

De volgende RTF-opdrachten worden genegeerd:

`\marg*`

## Tekst van vooraf formaat in pad {#section-ed492a8a54414cd4bde360500cec6968}

Indien `size=` wordt opgegeven samen met `textFlowPath=`, wordt de laaggrootte vooraf bepaald. (0,0) van de pixelcoördinaatruimte die wordt gebruikt om het pad of de paden te definiëren, bevindt zich in de linkerbovenhoek van de laagrechthoek.

De `textFlowPath=` gebieden kunnen zich buiten de laagrechthoek bevinden. Tekst wordt altijd in alle padgebieden laten doorlopen en gerenderd, zelfs als dit ertoe leidt dat tekst buiten de laagrechthoek wordt weergegeven. `extend=0,0,0,0`U kunt de gerenderde tekst uitsnijden naar de laagrechthoek.

Voor laagpositioneringsdoeleinden is de laagrechthoek gebaseerd op de opgegeven `size=`, ongeacht hoeveel tekst wordt gerenderd, zelfs als een deel ervan zich buiten de laagrechthoek bevindt. Standaardlaagpositionering is van toepassing.

`color=` Hiermee vult u het rechthoekige gebied dat wordt gedefinieerd door `size=`.

De volgende RTF-opdrachten worden genegeerd voor `textFlowPath=`:

`\marg*`

## Tekst op pad automatisch vergroten/verkleinen {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definieert een of meer paden waarin tekst is opgegeven met `textPs=` moet worden weergegeven. Wanneer `size=` niet wordt opgegeven, wordt de resulterende tekstlaag zichzelf aangepast. De laaggrootte wordt bepaald door het selectiekader van de werkelijke tekst die wordt gerenderd.

Als geen van beide `origin=` noch `anchor=` opgegeven, wordt voor het laaganker standaard (0,0) van de pixelcoördinaatruimte ingesteld die wordt gebruikt om het pad te definiëren; de positie van de gerenderde tekst is vast, ongeacht de hoeveelheid tekst die wordt gerenderd. Indien `anchor=` of `origin=` worden opgegeven, wordt de laag ten opzichte van (en aangepast aan) het selectiekader van de daadwerkelijk gerenderde inhoud geplaatst.

`color=` Hiermee vult u het selectiekader van de werkelijke tekst die wordt weergegeven.

De volgende RTF-opdrachten worden genegeerd:

* `\marg*`
* `\hyph*`
* `\vertal*`

Alle tekst na de eerste `\par` of `\line` wordt genegeerd.

## Tekst van vooraf formaat op pad {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Indien `size=` wordt opgegeven samen met `textPath=`, wordt de laaggrootte vooraf bepaald. (0,0) van de pixelcoördinaatruimte die wordt gebruikt om het pad of de paden te definiëren, bevindt zich in de linkerbovenhoek van de laagrechthoek.

De paden kunnen zich geheel of gedeeltelijk buiten de laagrechthoek bevinden. Tekst wordt altijd toegepast en weergegeven langs het gehele pad, zelfs buiten de laagrechthoek. `extend=0,0,0,0` U kunt de gerenderde tekst uitsnijden naar de laagrechthoek.

Voor laagpositioneringsdoeleinden is de laagrechthoek gebaseerd op de opgegeven `size=`, zelfs als een deel van de tekst buiten de laagrechthoek wordt weergegeven. Standaardlaagpositionering is van toepassing.

`color=` vult het gebied dat wordt gedefinieerd door `size=`.

De volgende RTF-opdrachten worden genegeerd:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Alle tekst na de eerste `\par` of `\line` wordt genegeerd.
