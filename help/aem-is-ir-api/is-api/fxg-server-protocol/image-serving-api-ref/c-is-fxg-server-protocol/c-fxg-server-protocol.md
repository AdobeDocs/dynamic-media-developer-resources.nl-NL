---
title: FXG-serverprotocol
description: Als u een afbeelding wilt bewerken, kunt u referentiepunten gebruiken die vergelijkbaar zijn met kompaspunten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FXG-serverprotocol{#fxg-server-protocol}

Als u een afbeelding wilt bewerken, kunt u referentiepunten gebruiken die vergelijkbaar zijn met kompaspunten.

Met behulp van referentiepunten kunt u een afbeelding roteren, schalen of de grootte ervan wijzigen ten opzichte van een bepaald referentiepunt. De referentiepunten zijn `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` en `southeast`. Als u bijvoorbeeld het middelste referentiepunt gebruikt, kunt u een afbeelding 45° roteren in het midden. In de volgende afbeelding ziet u waar de referentiepunten zich bevinden, een afbeelding, de afbeelding 20° gedraaid ten opzichte van het referentiepunt `northWest` en de afbeelding 20° gedraaid ten opzichte van het referentiepunt `east`.

![Afbeelding referentiepunten](assets/wp_ref_points.png)

* A. Locatie referentiepunt
* B. Een afbeelding
* C. De afbeelding is 20° gedraaid ten opzichte van het referentiepunt `northWest`
* D. De afbeelding is 20° geroteerd ten opzichte van het referentiepunt `east`

De syntaxis is:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

De standaardwaarde is geen. De waarde `inherit` geeft de waarde `s7:referencePoint` door, op voorwaarde dat deze waarde niet `none` is, vanaf de bovenkant van de pagina of het groepsniveau tot alle onderliggende items. Met de instelling `none` is er geen referentiepunt voor het object en wordt het FXG-coördinatensysteem gebruikt.

>[!NOTE]
>
>Als u een referentiepunt wilt gebruiken en geen verschuiving in het object wilt toepassen nadat het is gemanipuleerd, werkt u de x- en y-waarden van het object bij nadat u het hebt bewerkt.

Wanneer een waarde van `s7:referencePoint` wordt gebruikt met groepen (of wegen, lijnelementen, of om het even welk element dat geen expliciete breedte en hoogtedefinities heeft), is de waarde van toepassing op het cumulatieve bounding vakje van de groep. Het punt linksboven van het selectiekader van alle objecten in de groep fungeert bijvoorbeeld als referentiepunt `northWest` voor de groep; het punt rechtsonder fungeert als referentiepunt `southEast`.
