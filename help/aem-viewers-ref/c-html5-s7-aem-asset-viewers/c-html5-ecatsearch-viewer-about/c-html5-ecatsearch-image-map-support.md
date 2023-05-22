---
description: De zoekviewer voor eCatalog ondersteunt het renderen van pictogrammen voor afbeeldingen met hyperlinks boven de hoofdweergave.
solution: Experience Manager
title: Ondersteuning voor afbeeldingen met hyperlinks
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Ondersteuning voor afbeeldingen met hyperlinks{#image-map-support}

De zoekviewer voor eCatalog ondersteunt het renderen van pictogrammen voor afbeeldingen met hyperlinks boven de hoofdweergave.

De vormgeving van kaartpictogrammen wordt bepaald door CSS, zoals beschreven in [Afbeeldingskaart, effect](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Met afbeeldingen met hyperlinks voert u een van de volgende drie handelingen uit: omleiden naar een externe webpagina, pop-upactivering van het deelvenster Info en interne hyperlinks.

## Omleiden naar een externe webpagina {#section-32ebe3c3a7f74892a428c5d48801de4d}

De `href` kenmerk van de afbeelding met hyperlinks heeft een URL naar de externe bron, expliciet opgegeven of opgenomen in een van de ondersteunde JavaScript-sjabloonfuncties: `loadProduct()`, `loadProductCW()`, en `loadProductPW()`.

Hieronder ziet u een voorbeeld van een eenvoudige URL-omleiding:

`href=http://www.adobe.com`

In dit voorbeeld wordt dezelfde URL omsloten met de `loadProduct()` functie:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Houd er rekening mee dat wanneer u de JavaScript-code toevoegt aan de `HREF` kenmerk van de afbeelding met hyperlinks, wordt de code uitgevoerd op de computer van de client. Controleer daarom of de JavaScript-code veilig is.

## Pop-upactivering deelvenster Info {#section-7aa036420af646d1ad8cdc388add0b57}

Als u met de deelvensters Info wilt werken, heeft een afbeeldingskaart de opdracht `ROLLOVER_KEY` kenmerkset. Stel ook de `href` als de verwerking van de externe URL invloed heeft op de pop-upactivering van het deelvenster Info.

Tot slot moet u ervoor zorgen dat de viewerconfiguratie de juiste waarden bevat voor `InfoPanelPopup.template` en eventueel `InfoPanelPopup.infoServerUrl` parameters.

>[!NOTE]
>
>Houd er rekening mee dat wanneer u de pop-up van het deelvenster Info configureert, de HTML-code en JavaScript-code die aan het deelvenster Info worden doorgegeven, op de computer van de client worden uitgevoerd. Controleer daarom of dergelijke HTML-code en JavaScript-code veilig zijn.

## Interne hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Als u op een afbeelding met hyperlinks klikt, wordt er een interne pagina-omwisseling binnen de viewer uitgevoerd. Als u die functie wilt gebruiken, `href` heeft het kenmerk in de afbeelding met hyperlinks de volgende speciale indeling:

` href=target: *`idx`*`

waar `*`idx`*` is een op nul gebaseerde index van de catalogusspread.

Hieronder ziet u een voorbeeld van een `href` kenmerk voor een afbeelding met hyperlinks die wijst naar de 3D-spread in de eCatalog:

`href=target:2`
