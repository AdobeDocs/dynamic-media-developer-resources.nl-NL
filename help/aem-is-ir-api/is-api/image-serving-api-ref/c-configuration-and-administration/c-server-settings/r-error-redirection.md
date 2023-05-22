---
description: Gebruik deze serverinstellingen om fouten om te leiden.
solution: Experience Manager
title: Fout bij omleiden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
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

Maximale tijd (in msec) waarop de server wacht tot een verbinding met de secundaire server tot stand is gebracht voordat een fout naar de client wordt geretourneerd.

## PS::errorRedirect.socketTimeout - Redirect Timeout van de Reactie {#section-69d8579f748d4044bca99dfb64dd523c}

Maximale tijd (in msec) de server zal op de secundaire server wachten om gegevens terug te keren alvorens het omleidingsverzoek te verlaten en een fout aan de cliënt terug te keren.
