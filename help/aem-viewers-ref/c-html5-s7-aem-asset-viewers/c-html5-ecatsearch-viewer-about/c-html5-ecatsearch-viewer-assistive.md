---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-title: Technische ondersteuning
solution: Experience Manager
title: Technische ondersteuning
topic: Dynamic media
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---


# Support voor ondersteunende hulpmiddelen{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft het kenmerk rol `region` en `aria-label` standaard ingesteld op de naam van de viewer. U kunt het label besturen met het lokalisatiesymbool `Container.LABEL`.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met het kenmerk `aria-label`. De waarde van het kenmerk `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knoop gehandicapt is, wordt `aria-disabled` attributen geplaatst dienovereenkomstig.

De hoofdweergave heeft de rol `application`. Een korte beschrijving van de hoofdweergave vindt u in `aria-roledescription`, met de waarde die wordt gedefinieerd door het lokalisatiesymbool `ROLE_DESCRIPTION` van de overeenkomstige hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden opgegeven met `aria-describedby`. De tekst voor de gebruikshint is afkomstig van het `USAGE_HINT`-lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt het kenmerk `aria-label` ingesteld met de waarde van een dergelijk label.

Hot spots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met het kenmerk `aria-label`, met de waarde van de hotspot of het label van de afbeeldingskaart. Wanneer de gebruiker focus op hotspots of afbeeldingen met hyperlinks plaatst, worden navigatietekens voor toetsenbordgebruikers opgegeven met `aria-describedby`, waarbij de tekst voor de gebruikshint afkomstig is van het `USAGE_HINT`-lokalisatiesymbool.

Miniaturen hebben de rol `dialog` met `aria-label` attribuut dat door het `ThumbnailGridView.LABEL` localisatiesymbool wordt gecontroleerd. Afzonderlijke miniaturen hebben de rol `button`. Als een miniatuur is geselecteerd, wordt `aria-selected`-kenmerk ingesteld op `true`.

Componenten die stalen weergeven, hebben de rol `listbox` met `aria-label` kenmerk ingesteld op de waarde van het `LABEL` lokalisatiesymbool van die component. Afzonderlijke stalen hebben de rol `option` met de kenmerken `aria-setsize` en `aria-posinset` om de staalpositie in de set te beschrijven. Als een staal is geselecteerd, krijgt het kenmerk `aria-selected` ingesteld op `true`.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra `aria-haspopup`-kenmerk ingesteld op `true` en het `aria-controls`-kenmerk dat verwijst naar het daadwerkelijke element van het vervolgkeuzevenster. Het vervolgkeuzevenster heeft de rol `menu` met subelementen die de rol `menuitem` hebben. Voor elk menu-item wordt het kenmerk `aria-label` opgegeven.

De gebruikersinterface van het onderzoek wordt gegroepeerd in het element met de rol `search`. Het veld Invoerveld zoeken heeft de rol `searchbox` en verwijst naar het informatieve label dat wordt beheerd door het localisatiesymbool `SearchPanel.INFO_PROMPT` met het kenmerk `aria-describedby`.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt verwezen door het kenmerk `aria-labelledby`.
