---
title: Meerdere verlichtingstoewijzingen gebruiken
description: Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Meerdere verlichtingstoewijzingen gebruiken{#using-multiple-illumination-maps}

Voor sommige toepassingen is mogelijk een andere verlichtingskaart voor verschillende soorten materialen vereist.

Voor elk vignet kunnen maximaal drie verlichtingstoewijzingen worden gemaakt. De verlichtingskaart voor een renderbewerking wordt geselecteerd met de `illum=` en of `gloss=` opdrachten.

**Standaardselectie** - Indien `illum=` of `gloss=` niet worden opgegeven, gebruikt de renderer de eerste gemaakte verlichtingskaart (normaal kaart A, ook wel de &#39;Plat&#39;-verlichtingskaart genoemd).

**Automatische selectie met`gloss=`** - Indien `illum=` is niet opgegeven of is ingesteld op `-1`, vergelijkt de renderer de opgegeven waarden `gloss=` waarde met de glanswaarden die aan elke verlichtingsafbeelding in het vignet zijn gekoppeld. Hierbij wordt de verlichtingsafbeelding gekozen waarvan de glanswaarde het dichtst bij de opgegeven waarde ligt `gloss=`.

**Selectie expliciet maken met`illum=`** - Indien `illum=` is opgegeven en ingesteld op `0`, `1`, of `2`gebruikt de renderer de overeenkomstige verlichtingskaart; `gloss=` wordt genegeerd voor het selecteren van de verlichtingskaart.

Als het vignet slechts één verlichtingskaart bevat, gebruikt renderer die kaart en negeert `illum=` en `gloss=` opdrachten.
