---
description: 'null'
seo-description: 'null'
seo-title: Transformatie weergeven voor afbeeldingen
solution: Experience Manager
title: Transformatie weergeven voor afbeeldingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Transformatie weergeven voor afbeeldingen{#view-transform-for-images}

Het beeld dat als reactie op een `req=img` verzoek aan de cliënt wordt teruggegeven wordt afgeleid uit het samengestelde beeld door de volgende waarden te overwegen: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` en de grootte van de samengestelde afbeelding.

Als `wid=` en `hei=` worden gespecificeerd, en `scl=` niet is, wordt het samengestelde beeld geschraapt zodat het volledig binnen de meningsrect past die door `wid=` en `hei=` wordt bepaald. Als de hoogte-breedteverhouding van het weergaverect anders is dan die van de samengestelde afbeelding, wordt de geschaalde samengestelde afbeelding binnen het weergaverect uitgelijnd met de waarde `align=`, indien opgegeven, of anders gecentreerd. Elke ruimte die niet door afbeeldingsgegevens wordt gedekt, wordt gevuld met `bgc=` of, indien niet opgegeven, met `attribute::BkgColor`.

Wanneer `scl=` is opgegeven, wordt de samengestelde afbeelding met die schaalfactor geschaald. Als `wid=` en/of `hei=` eveneens wordt gespecificeerd, wordt het geschraapte beeld dan uitgesneden aan `wid=` en/of `hei=` of extra ruimte toegevoegd, zoals nodig. `align=` Hiermee geeft u aan waar de afbeelding wordt uitgesneden of extra ruimte wordt toegevoegd en eventuele extra ruimte wordt gevuld met  `bgc=` of  `attribute::BkgColor`.

Als noch `wid=`, `hei=` noch `scl=` worden gespecificeerd, en als of breedte of hoogte van het samengestelde beeld `attribute::DefaultPix` overschrijdt, wordt het samengestelde beeld geschraapt om `attribute::DefaultPix` niet te overschrijden. Anders wordt de samengestelde afbeelding gebruikt zonder te schalen.

Geef `scl=1` op om ervoor te zorgen dat de weergaveafbeelding wordt geretourneerd zonder verdere schaling.

Als `rgn=` wordt gespecificeerd, wordt het antwoordbeeld dan aangepast om de definitieve grootte van het antwoordbeeld te bereiken. Deze grootte wordt vergeleken met `attribute::MaxPix` (als bepaald), en een fout wordt geproduceerd als het antwoordbeeld in één van beide afmeting groter is.

Als `fmt=` gegevens zonder alpha specificeert, worden om het even welke transparante gebieden in het antwoordbeeld gevuld met `bgc=` of `attribute::BkgColor`.
