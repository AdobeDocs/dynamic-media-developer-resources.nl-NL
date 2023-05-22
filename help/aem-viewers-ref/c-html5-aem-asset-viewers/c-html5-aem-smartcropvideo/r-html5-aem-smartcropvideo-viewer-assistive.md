---
title: Technische ondersteuning
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft een rol `region` en `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, `aria-disabled` wordt dienovereenkomstig ingesteld.

De component Slider heeft de rol `slider` met kenmerken `aria-valuenow`, `aria-valuemin`, en `aria-valuemax` om de huidige schuifregelaarpositie te beschrijven.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra opties `aria-haspopup` kenmerk ingesteld op `true` en `aria-controls` kenmerk dat verwijst naar het daadwerkelijke element in het vervolgkeuzevenster. De rol van het vervolgkeuzevenster zelf is `menu` met subelementen die een rol spelen `menuitem`. Elk menu-item heeft de `aria-label` opgegeven kenmerk.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt verwezen door het `aria-labelledby` kenmerk.
