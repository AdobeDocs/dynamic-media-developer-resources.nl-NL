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

---


# Transformatie weergeven voor afbeeldingen{#view-transform-for-images}

Het beeld dat als antwoord op een `req=img` verzoek aan de cliënt wordt teruggegeven wordt afgeleid uit het samengestelde beeld door de volgende waarden te overwegen: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`en de grootte van de samengestelde afbeelding.

Als `wid=` en `hei=` worden gespecificeerd, en `scl=` is niet, wordt het samengestelde beeld geschraapt zodat het volledig binnen de meningsrect past die door `wid=` en `hei=`wordt bepaald. Als de hoogte-breedteverhouding van de weergaverechthoek verschilt van die van de samengestelde afbeelding, wordt de geschaalde samengestelde afbeelding binnen de weergaverechthoek uitgelijnd met de opgegeven `align=` waarde, of anders gecentreerd. Elke ruimte die niet door afbeeldingsgegevens wordt bedekt, wordt gevuld met `bgc=` of, indien niet opgegeven, met `attribute::BkgColor`.

Als `scl=` dit het geval is, wordt de samengestelde afbeelding met die schaalfactor geschaald. Als `wid=` en/of `hei=` ook wordt opgegeven, wordt de geschaalde afbeelding uitgesneden tot `wid=` en/of `hei=` of wordt zo nodig extra ruimte toegevoegd. `align=` Hiermee geeft u aan waar de afbeelding wordt uitgesneden of extra ruimte wordt toegevoegd en eventuele extra ruimte wordt gevuld met `bgc=` of `attribute::BkgColor`.

Als noch `wid=`, `hei=` noch `scl=` gespecificeerd, en of breedte of hoogte van het samengestelde beeld overschrijdt `attribute::DefaultPix`, wordt het samengestelde beeld geschraapt om niet te overschrijden `attribute::DefaultPix`. Anders wordt de samengestelde afbeelding gebruikt zonder te schalen.

Geef op om ervoor te zorgen dat de weergaveafbeelding wordt geretourneerd zonder verdere schaling. `scl=1`Geef dit op.

Als `rgn=` is opgegeven, wordt de antwoordafbeelding vervolgens bijgesneden om de uiteindelijke afbeeldingsgrootte van de reactie te verkrijgen. Deze grootte wordt vergeleken met `attribute::MaxPix` (indien gedefinieerd) en er wordt een fout gegenereerd als de antwoordafbeelding in een van beide dimensies groter is.

Als `fmt=` u gegevens zonder alfa opgeeft, worden transparante gebieden in de antwoordafbeelding gevuld met `bgc=` of `attribute::BkgColor`.
