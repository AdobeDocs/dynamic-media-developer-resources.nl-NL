---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
title: Technische ondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's,Toegankelijkheid
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Support voor ondersteunende hulpmiddelen{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft het kenmerk rol `region` en `aria-label` standaard ingesteld op de naam van de viewer. U kunt het label besturen met het lokalisatiesymbool `Container.LABEL`.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van het kenmerk `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knoop gehandicapt is, `aria-disabled` wordt attributen geplaatst dienovereenkomstig.

De componenten van de schuif hebben de rol `slider` met attributen `aria-valuenow`, `aria-valuemin`, en `aria-valuemax` om de huidige schuif positie te beschrijven.

Miniaturen hebben de rol `dialog` met `aria-label` attribuut dat door het `ThumbnailGridView.LABEL` localisatiesymbool wordt gecontroleerd. Afzonderlijke miniaturen hebben de rol `button`. Als een miniatuur is geselecteerd, wordt `aria-selected`-kenmerk ingesteld op `true`.

Componenten die stalen weergeven, hebben de rol `listbox` met `aria-label` kenmerk ingesteld op de waarde van het `LABEL` lokalisatiesymbool van die component. Afzonderlijke stalen hebben de rol `option` met de kenmerken `aria-setsize` en `aria-posinset` om de staalpositie in de set te beschrijven. Als een staal is geselecteerd, krijgt het kenmerk `aria-selected` ingesteld op `true`.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra `aria-haspopup`-kenmerk ingesteld op `true` en `aria-controls`-kenmerk dat verwijst naar het daadwerkelijke element van het vervolgkeuzevenster. Het vervolgkeuzevenster heeft de rol `menu` met subelementen die de rol `menuitem` hebben. Voor elk menu-item wordt het kenmerk `aria-label` opgegeven.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt verwezen door het kenmerk `aria-labelledby`.
