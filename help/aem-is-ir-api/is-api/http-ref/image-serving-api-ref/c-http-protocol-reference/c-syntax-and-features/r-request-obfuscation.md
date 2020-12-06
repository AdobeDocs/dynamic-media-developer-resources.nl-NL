---
description: De inhoud van het volledige modifiers-gedeelte van de aanvraagtekenreeks, inclusief het optionele vergrendelingsachtervoegsel, kan worden verborgen door het toepassen van standaard base64-codering.
seo-description: De inhoud van het volledige modifiers-gedeelte van de aanvraagtekenreeks, inclusief het optionele vergrendelingsachtervoegsel, kan worden verborgen door het toepassen van standaard base64-codering.
seo-title: Vragen om verwarring
solution: Experience Manager
title: Vragen om verwarring
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Vragen om verwarring{#request-obfuscation}

De inhoud van het volledige modifiers-gedeelte van de aanvraagtekenreeks, inclusief het optionele vergrendelingsachtervoegsel, kan worden verborgen door het toepassen van standaard base64-codering.

De server probeert te decoderen als deze `attribute::RequestObfuscation` is ingesteld. Indien decodering mislukt, wordt het verzoek afgewezen. Als zowel de verzoekvergrendeling als de verzoekverwarring worden toegepast, moet het slotachtervoegsel worden geproduceerd en toegevoegd vóór base64 het coderen.

>[!IMPORTANT]
>
>Als u deze functie inschakelt, dient u er rekening mee te houden dat er bepaalde gebruiksbeperkingen zijn, waaronder de volgende:<br>- De gebruikersinterface Dynamische media geeft mogelijk niet de juiste details voor het **[!UICONTROL Last Published]** veld weer. Dit heeft echter geen invloed op de uitgeverij.<br>- HLS-videostreaming werkt momenteel niet wanneer **[!UICONTROL Request obfuscation]** en **[!UICONTROL Request locking]** wordt ingeschakeld.<br>- Momenteel werken sommige Dynamic Media Viewers niet wanneer **[!UICONTROL Request obfuscation]** en **[!UICONTROL Request locking]** worden ingeschakeld.

## Voorbeeld {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

coderen naar:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Elke keer dat &#39;=&#39;, &#39;&amp;&#39; en &#39;%&#39; in waardetekenreeksen voorkomt, moet met de codering &#39;%xx&#39; worden gewist voordat de aanvraag wordt verduisterd. Het is niet noodzakelijk om het *modifiers* deel van het verzoek of vóór of na obfuscation anders te coderen, zelfs als verzoek het sluiten wordt toegepast, aangezien base64 het coderen voor HTTP transmissie veilig is.

## Zie ook {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Locking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
