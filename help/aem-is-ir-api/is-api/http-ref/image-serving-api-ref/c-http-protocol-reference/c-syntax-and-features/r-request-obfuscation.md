---
description: De inhoud van het volledige modifiers-gedeelte van de aanvraagtekenreeks, inclusief het optionele vergrendelingsachtervoegsel, kan worden verborgen door het toepassen van standaard base64-codering.
solution: Experience Manager
title: Vragen om verwarring
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Vragen om verwarring{#request-obfuscation}

De inhoud van het volledige modifiers-gedeelte van de aanvraagtekenreeks, inclusief het optionele vergrendelingsachtervoegsel, kan worden verborgen door het toepassen van standaard base64-codering.

De server probeert te decoderen als `attribute::RequestObfuscation` is ingesteld. Indien decodering mislukt, wordt het verzoek afgewezen. Als zowel de verzoekvergrendeling als de verzoekverwarring worden toegepast, moet het slotachtervoegsel worden geproduceerd en toegevoegd vóór base64 het coderen.

>[!IMPORTANT]
>
>Als u deze functie inschakelt, moet u er rekening mee houden dat er bepaalde gebruiksbeperkingen zijn, waaronder:<br>- De Dynamic Media-gebruikersinterface bevat mogelijk niet de juiste gegevens voor de **[!UICONTROL Last Published]** veld. Dit heeft echter geen invloed op de uitgeverij.<br>- HLS-videostreaming werkt momenteel niet wanneer **[!UICONTROL Request obfuscation]** en **[!UICONTROL Request locking]** zijn ingeschakeld.<br>- Sommige Dynamic Media Viewers werken momenteel niet wanneer **[!UICONTROL Request obfuscation]** en **[!UICONTROL Request locking]** zijn ingeschakeld.

## Voorbeeld {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

coderen naar:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Elke keer dat &#39;=&#39;, &#39;&amp;&#39; en &#39;%&#39; in waardetekenreeksen voorkomt, moet met de codering &#39;%xx&#39; worden gewist voordat de aanvraag wordt verduisterd. Het is niet nodig om anders http-encode te coderen *modifiers* een deel van het verzoek of vóór of na obfuscatie, zelfs als de verzoeksluiting wordt toegepast, aangezien base64 het coderen voor HTTP transmissie veilig is.

## Zie ook {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-codering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Verzoek vergrendelen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [kenmerk::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
