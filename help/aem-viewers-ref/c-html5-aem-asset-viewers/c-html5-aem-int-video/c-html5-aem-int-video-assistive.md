---
title: Technische ondersteuning
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft een rol `region` en `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, `aria-disabled` wordt dienovereenkomstig ingesteld.

De component Slider heeft de rol `slider` met kenmerken `aria-valuenow`, `aria-valuemin`, en `aria-valuemax` om de huidige schuifregelaarpositie te beschrijven.

Miniaturen hebben de rol `dialog` with `aria-label` door de `ThumbnailGridView.LABEL` lokalisatiesymbool. Afzonderlijke miniaturen hebben een rol `button`. Als er een miniatuur is geselecteerd, wordt deze weergegeven `aria-selected` kenmerk ingesteld op `true`.

Componenten die stalen weergeven, hebben de rol `listbox` with `aria-label` kenmerk ingesteld op de waarde van het `LABEL` lokalisatiesymbool van die component. Afzonderlijke stalen hebben de rol `option` with `aria-setsize` en `aria-posinset` kenmerken die de staalpositie in de set beschrijven. Als er een staal is geselecteerd, worden de `aria-selected` kenmerk ingesteld op `true`.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra opties `aria-haspopup` kenmerk ingesteld op `true` en `aria-controls` kenmerk dat verwijst naar het daadwerkelijke element in het vervolgkeuzevenster. De rol van het vervolgkeuzevenster zelf is `menu` met subelementen die een rol spelen `menuitem`. Elk menu-item heeft de `aria-label` opgegeven kenmerk.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt verwezen door het `aria-labelledby` kenmerk.
