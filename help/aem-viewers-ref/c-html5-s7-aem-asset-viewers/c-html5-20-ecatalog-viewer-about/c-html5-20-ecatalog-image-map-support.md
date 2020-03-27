---
description: De eCatalog-viewer ondersteunt het renderen van pictogrammen voor afbeeldingen met hyperlinks boven de hoofdweergave.
seo-description: De eCatalog-viewer ondersteunt het renderen van pictogrammen voor afbeeldingen met hyperlinks boven de hoofdweergave.
seo-title: Ondersteuning voor afbeeldingen met hyperlinks
solution: Experience Manager
title: Ondersteuning voor afbeeldingen met hyperlinks
topic: Dynamic media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ondersteuning voor afbeeldingen met hyperlinks{#image-map-support}

De eCatalog-viewer ondersteunt het renderen van pictogrammen voor afbeeldingen met hyperlinks boven de hoofdweergave.

De vormgeving van kaartpictogrammen wordt bepaald door CSS, zoals beschreven in het [afbeeldingskaarteffect](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Met afbeeldingen met hyperlinks voert u een van de volgende drie handelingen uit: omleiden naar een externe webpagina, pop-upactivering van het deelvenster Info en interne hyperlinks.

## Omleiden naar een externe webpagina {#section-32ebe3c3a7f74892a428c5d48801de4d}

Het `href` kenmerk van de afbeelding met hyperlinks heeft een URL naar de externe bron, expliciet opgegeven of opgenomen in een van de ondersteunde JavaScript-sjabloonfuncties: `loadProduct()`, `loadProductCW()`, en `loadProductPW()`.

Hieronder ziet u een voorbeeld van een eenvoudige URL-omleiding:

`href=http://www.adobe.com`

In dit voorbeeld wordt dezelfde URL omsloten met de `loadProduct()` functie:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Houd er rekening mee dat wanneer u de JavaScript-code toevoegt aan het `HREF` kenmerk van de afbeelding met hyperlinks, de code wordt uitgevoerd op de computer van de client. Controleer daarom of de JavaScript-code veilig is.

## Pop-upactivering deelvenster Info {#section-7aa036420af646d1ad8cdc388add0b57}

Als u met de deelvensters Info wilt werken, heeft een afbeelding met hyperlinks het `ROLLOVER_KEY` kenmerk ingesteld. Stel het `href` kenmerk ook tegelijkertijd in, anders reageert de externe URL-verwerking op de pop-upactivering van het deelvenster Info.

Tot slot zeker ben dat de kijkersconfiguratie de aangewezen waarden voor `InfoPanelPopup.template` en, naar keuze, `InfoPanelPopup.infoServerUrl` parameters omvat.

>[!NOTE]
>
>Houd er rekening mee dat wanneer u de pop-up van het deelvenster Info configureert, de HTML-code en de JavaScript-code die aan het deelvenster Info zijn doorgegeven, op de computer van de client worden uitgevoerd. Zorg daarom dat dergelijke HTML-code en JavaScript-code veilig zijn.

## Interne hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Als u op een afbeelding met hyperlinks klikt, wordt er een interne pagina-omwisseling binnen de viewer uitgevoerd. Als u die functie wilt gebruiken, heeft een `href` kenmerk in de afbeelding met hyperlinks de volgende speciale indeling:

` href=target: *`idx`*`

waarbij ` *`idx`*` een op nul gebaseerde index van de catalogusspread is.

Hieronder ziet u een voorbeeld van een `href` kenmerk voor een afbeelding met hyperlinks dat naar de 3D-spread in de eCatalog wijst:

`href=target:2`
