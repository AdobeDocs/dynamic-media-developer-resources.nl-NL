---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
title: Technische ondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Toegankelijkheid
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft het kenmerk rol `region` en `aria-label` standaard ingesteld op de naam van de viewer. U kunt het label besturen met het lokalisatiesymbool `Container.LABEL`.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van het kenmerk `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knoop gehandicapt is, `aria-disabled` wordt attributen geplaatst dienovereenkomstig.

De componenten van de schuif hebben de rol `slider` met attributen `aria-valuenow`, `aria-valuemin`, en `aria-valuemax` om de huidige schuif positie te beschrijven.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra `aria-haspopup`-kenmerk ingesteld op `true` en `aria-controls`-kenmerk dat verwijst naar het daadwerkelijke element van het vervolgkeuzevenster. Het vervolgkeuzevenster heeft de rol `menu` met subelementen die de rol `menuitem` hebben. Voor elk menu-item wordt het kenmerk `aria-label` opgegeven.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt verwezen door het kenmerk `aria-labelledby`.
