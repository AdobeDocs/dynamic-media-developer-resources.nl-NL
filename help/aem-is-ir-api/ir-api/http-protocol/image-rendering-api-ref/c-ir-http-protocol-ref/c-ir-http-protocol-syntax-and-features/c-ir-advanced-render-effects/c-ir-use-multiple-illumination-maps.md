---
description: Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.
seo-description: Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.
seo-title: Meerdere verlichtingstoewijzingen gebruiken
solution: Experience Manager
title: Meerdere verlichtingstoewijzingen gebruiken
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Meerdere verlichtingstoewijzingen gebruiken{#using-multiple-illumination-maps}

Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.

Voor elk vignet kunnen maximaal drie verlichtingstoewijzingen worden gemaakt. De verlichtingskaart voor een teruggeeft verrichting wordt geselecteerd met de `illum=` en of `gloss=` bevelen.

**Standaardselectie** Als er geen `illum=` of `gloss=` geen waarde is opgegeven, gebruikt de renderer de eerste geschreven verlichtingskaart (normaal gesproken kaart A, ook wel de &#39;Plat&#39;-verlichtingskaart genoemd).

**Automatische selectie met`gloss=`**Als`illum=`niet is opgegeven of is ingesteld op -1, vergelijkt de renderer de opgegeven`gloss=`waarde met de glanswaarden die zijn gekoppeld aan elke verlichtingsafbeelding in het vignet en kiest u de verlichtingsafbeelding waarvan de glanswaarde het dichtst bij de opgegeven waarde ligt`gloss=`.

**Expliciete selectie met`illum=`**Als`illum=`wordt gespecificeerd en aan 0, 1, of 2 wordt geplaatst, zal renderer de overeenkomstige verlichtingskaart gebruiken; wordt genegeerd voor het selecteren van de verlichtingskaart.`gloss=`

Als het vignet slechts één verlichtingskaart bevat, zal renderer die kaart gebruiken en de `illum=` en `gloss=` bevelen negeren.
