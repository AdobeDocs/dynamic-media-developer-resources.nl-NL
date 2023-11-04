---
description: Gebruik deze serverinstellingen om fouten om te leiden.
solution: Experience Manager
title: Fout bij omleiden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Fout bij omleiden{#error-redirection}

Gebruik deze serverinstellingen om fouten om te leiden.

>[!NOTE]
>
>Pijptekens (|) in het nettopad worden niet ondersteund voor het omleiden van fouten.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

De basis-URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) voor het secundaire Beeld dat plaatsing serveert waaraan de verzoeken die plaatselijk ontbreken zouden moeten worden opnieuw gericht. De omleiding van de fout is gehandicapt (gebrek) wanneer dit het plaatsen of niet bepaald leeg is.

## PS::errorRedirect.connectTimeout - Time-out voor omleiding van verbinding {#section-3971be8f720d4b32a2cc7860b4085971}

Maximale tijd (in msec) wacht de server op een verbinding met de secundaire server die moet worden ingesteld voordat een fout op de client wordt geretourneerd.

## PS::errorRedirect.socketTimeout - Redirect Timeout van de Reactie {#section-69d8579f748d4044bca99dfb64dd523c}

Maximale tijd (in msec) wacht de server op de secundaire server om gegevens terug te keren voordat de omleidingsaanvraag wordt verlaten en een fout op de client wordt geretourneerd.
