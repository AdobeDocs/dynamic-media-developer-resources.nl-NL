---
description: Maak een toepassing voor het in lagen plaatsen van een "papieren pop".
seo-description: Maak een toepassing voor het in lagen plaatsen van een "papieren pop".
seo-title: Voorbeeld C
solution: Experience Manager
title: Voorbeeld C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Voorbeeld C{#example-c}

Maak een toepassing voor het in lagen plaatsen van een &quot;papieren pop&quot;.

Een achtergrondafbeelding bevat de foto van een model of mannequin. Aanvullende records in de afbeeldingscatalogus bevatten verschillende kleding en accessoire-items die zijn gefotografeerd om overeen te komen met de vorm en grootte van de nequin.

Elke foto op het scherm of in het accessoire wordt gemaskeerd en uitgesneden tot het selectiekader van het masker om de afbeeldingsgrootte te minimaliseren. Ankerpunten en resoluties van afbeeldingen worden zorgvuldig geregeld om de uitlijning tussen de lagen en de achtergrondafbeelding te behouden en alle afbeeldingen worden toegevoegd aan een afbeeldingscatalogus, met de juiste waarden opgeslagen in `catalog::Resolution` en `catalog::Anchor`.

Naast lagen willen we ook de kleur van geselecteerde items wijzigen. De records voor deze items worden vooraf verwerkt om de oorspronkelijke kleur te verwijderen en de helderheid en het contrast aan te passen op een wijze die geschikt is voor de inkleuringsopdracht. Deze voorbehandeling kan offline worden uitgevoerd met een beeldbewerkingsprogramma zoals Photoshop of, in eenvoudige gevallen, triviaal worden uitgevoerd door `op_brightness=` en `op_contrast=` toe te voegen aan het `catalog::Modifier`veld.

Deze toepassing garandeert geen aparte sjabloon, omdat alle objecten al correct zijn uitgelijnd door hun afbeeldingsankers ( `catalog::Anchor`) en geschaald ( `catalog::Resolution`). Wij laten het aan de cliënt over om aangewezen laagorde te verzekeren.

Een typisch verzoek zou als dit kunnen kijken:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Alleen de hoogte wordt opgegeven. Hierdoor kan de breedte van de geretourneerde afbeelding variëren, afhankelijk van de hoogte-breedteverhouding van de hoofdafbeelding, zonder dat de marges worden gevuld met de achtergrondkleur.

Het maakt niet uit welke resolutie voor elke laag is opgegeven, zolang deze allemaal gelijk zijn. Deze versie staat mogelijk niet toe dat weergaven groter zijn dan de samengestelde afbeeldingen. Als u een hoge resolutiewaarde opgeeft, worden problemen met betrekking tot deze beperking voorkomen. Alle bewerkingen en composities worden uitgevoerd met de optimale resolutie voor de gewenste afbeeldingsgrootte, zodat u de beste prestaties en uitvoerkwaliteit krijgt.

De `res=`-opdrachten kunnen worden weggelaten als alle bronafbeeldingen dezelfde resolutie op volledige schaal hebben (wat waarschijnlijk het geval is voor dit type toepassing).

`rootId` moet voor alle `src=` bevelen worden gespecificeerd, zelfs als zij het zelfde zijn als `rootId` in de url weg wordt gespecificeerd.

Als er geen afbeeldingscatalogus moet worden gebruikt, is schalen op basis van resolutie niet mogelijk. In dit geval moeten expliciete schaalfactoren worden berekend voor elk laagitem, op basis van de verhouding tussen de `catalog::Resolution`-waarden voor elke laag en de `catalog::Resolution`-waarde van de achtergrondlaag. Het samenstellende verzoek (met minder lagen) zou zo kunnen kijken:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

