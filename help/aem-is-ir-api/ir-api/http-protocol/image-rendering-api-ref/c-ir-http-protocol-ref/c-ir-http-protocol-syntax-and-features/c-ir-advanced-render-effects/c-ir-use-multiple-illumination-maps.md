---
description: Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.
seo-description: Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.
seo-title: Meerdere verlichtingstoewijzingen gebruiken
solution: Experience Manager
title: Meerdere verlichtingstoewijzingen gebruiken
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Meerdere verlichtingstoewijzingen gebruiken{#using-multiple-illumination-maps}

Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.

Voor elk vignet kunnen maximaal drie verlichtingstoewijzingen worden gemaakt. De verlichtingskaart voor een teruggeeft verrichting wordt geselecteerd met `illum=` en of `gloss=` bevelen.

**Standaard** selectieAls noch  `illum=` noch  `gloss=` zijn gespecificeerd, zal renderer de eerste authored verlichtingskaart (typisch kaart A, ook wel &quot;Vlakke&quot;verlichtingskaart genoemd) gebruiken.

**Automatische selectie met`gloss=`** Als niet opgegeven of ingesteld  `illum=` is op -1, vergelijkt de renderer de opgegeven  `gloss=` waarde met de glanswaarden die aan elke verlichtingskaart in het vignet zijn gekoppeld, en kiest u de verlichtingskaart waarvan de glanswaarde het dichtst bij de opgegeven waarde ligt  `gloss=`.

**Expliciete selectie met`illum=`** Als  `illum=` wordt gespecificeerd en aan 0, 1, of 2 wordt geplaatst, zal renderer de overeenkomstige verlichtingskaart gebruiken;  `gloss=` wordt genegeerd voor het selecteren van de verlichtingskaart.

Als het vignet slechts één verlichtingskaart bevat, zal renderer die kaart gebruiken en zal `illum=` en `gloss=` bevelen negeren.
