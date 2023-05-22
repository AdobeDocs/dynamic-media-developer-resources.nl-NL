---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
title: Technische ondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft een rol `region` en `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met de `aria-label` kenmerk. De waarde van `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, wordt `aria-disabled` wordt dienovereenkomstig ingesteld.

De hoofdweergave heeft een rol `application`. Een korte beschrijving van het hoofdstandpunt wordt gegeven in `aria-roledescription`met de waarde die door de `ROLE_DESCRIPTION` lokalisatiesymbool van de bijbehorende hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden weergegeven met `aria-describedby`, de tekst voor de gebruikstip afkomstig is van de `USAGE_HINT` lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt `aria-label` wordt ingesteld met de waarde van een dergelijk label.

Hotspots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` met de waarde van de hotspot of het label van de afbeelding met hyperlinks. Wanneer de gebruiker de focus op hotspots of afbeeldingen met hyperlinks plaatst, worden navigatietekens voor toetsenbordgebruikers weergegeven met `aria-describedby`, met de tekst voor de gebruiksaanwijzing die afkomstig is van de `USAGE_HINT` lokalisatiesymbool.

Miniaturen hebben de rol `dialog` with `aria-label` door de `ThumbnailGridView.LABEL` lokalisatiesymbool. Afzonderlijke miniaturen hebben een rol `button`. Als er een miniatuur is geselecteerd, wordt deze weergegeven `aria-selected` kenmerk ingesteld op `true`.

Componenten die stalen weergeven, hebben de rol `listbox` with `aria-label` kenmerk ingesteld op de waarde van het `LABEL` lokalisatiesymbool van die component. Afzonderlijke stalen hebben de rol `option` with `aria-setsize` en `aria-posinset` kenmerken die de staalpositie in de set beschrijven. Als er een staal is geselecteerd, wordt het staal `aria-selected` kenmerk ingesteld op `true`.

Vervolgkeuzelijsten worden geactiveerd door knoppen met extra opties `aria-haspopup` kenmerk ingesteld op `true` en de `aria-controls` kenmerk dat verwijst naar het daadwerkelijke element in het vervolgkeuzevenster. De rol van het vervolgkeuzevenster zelf is `menu` met subelementen die een rol spelen `menuitem`. Elk menu-item heeft de `aria-label` opgegeven kenmerk.

De gebruikersinterface van het onderzoek wordt gegroepeerd in het element met de rol `search`. Het veld Zoeken in invoerveld heeft de rol `searchbox` en verwijst naar het informatieve label dat wordt beheerd door `SearchPanel.INFO_PROMPT` lokalisatiesymbool met `aria-describedby` kenmerk.

Modal dialoogvensters hebben de rol `dialog`. Naar het headerelement van het dialoogvenster wordt verwezen door het `aria-labelledby` kenmerk.
