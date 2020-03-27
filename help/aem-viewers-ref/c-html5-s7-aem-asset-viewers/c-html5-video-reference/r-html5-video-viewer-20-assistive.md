---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-title: Technische ondersteuning
solution: Experience Manager
title: Technische ondersteuning
topic: Dynamic media
uuid: e7090fb1-9458-4f97-a11f-5b0600a13db0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Voor het viewerelement op het hoogste niveau zijn de rol `region` en het `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van het `aria-label` kenmerk wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, wordt het `aria-disabled` kenmerk dienovereenkomstig ingesteld.

De componenten van de schuif hebben de rol `slider` met attributen `aria-valuenow`, `aria-valuemin`en `aria-valuemax` om de huidige schuifbalkpositie te beschrijven.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra `aria-haspopup` kenmerk ingesteld op `true` en `aria-controls` kenmerk dat verwijst naar het daadwerkelijke element van het vervolgkeuzevenster. Het vervolgkeuzevenster zelf heeft de rol `menu` met subelementen die de rol hebben `menuitem`. Elk menu-item heeft het opgegeven `aria-label` kenmerk.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt door het `aria-labelledby` kenmerk verwezen.
