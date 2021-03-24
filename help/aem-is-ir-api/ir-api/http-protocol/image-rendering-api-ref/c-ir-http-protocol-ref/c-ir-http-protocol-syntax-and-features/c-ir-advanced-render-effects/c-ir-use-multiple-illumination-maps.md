---
description: Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.
solution: Experience Manager
title: Meerdere verlichtingstoewijzingen gebruiken
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Meerdere verlichtingstoewijzingen gebruiken{#using-multiple-illumination-maps}

Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.

Voor elk vignet kunnen maximaal drie verlichtingstoewijzingen worden gemaakt. De verlichtingskaart voor een teruggeeft verrichting wordt geselecteerd met `illum=` en of `gloss=` bevelen.

**Standaard** selectieAls noch  `illum=` noch  `gloss=` zijn gespecificeerd, zal renderer de eerste authored verlichtingskaart (typisch kaart A, ook wel &quot;Vlakke&quot;verlichtingskaart genoemd) gebruiken.

**Automatische selectie met`gloss=`** Als niet opgegeven of ingesteld  `illum=` is op -1, vergelijkt de renderer de opgegeven  `gloss=` waarde met de glanswaarden die aan elke verlichtingskaart in het vignet zijn gekoppeld, en kiest u de verlichtingskaart waarvan de glanswaarde het dichtst bij de opgegeven waarde ligt  `gloss=`.

**Expliciete selectie met`illum=`** Als  `illum=` wordt gespecificeerd en aan 0, 1, of 2 wordt geplaatst, zal renderer de overeenkomstige verlichtingskaart gebruiken;  `gloss=` wordt genegeerd voor het selecteren van de verlichtingskaart.

Als het vignet slechts één verlichtingskaart bevat, zal renderer die kaart gebruiken en zal `illum=` en `gloss=` bevelen negeren.
