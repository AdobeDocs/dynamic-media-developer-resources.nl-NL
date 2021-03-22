---
description: Gebruik deze serverinstellingen om fouten om te leiden.
seo-description: Gebruik deze serverinstellingen om fouten om te leiden.
seo-title: Fout bij omleiden
solution: Experience Manager
title: Fout bij omleiden
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Fout bij omleiding{#error-redirection}

Gebruik deze serverinstellingen om fouten om te leiden.

>[!NOTE]
>
>Pijptekens (|) in het nettopad worden niet ondersteund voor het omleiden van fouten.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

De basis-URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) voor de secundaire implementatie van ImageServing waarbij aanvragen die lokaal mislukken, moeten worden omgeleid. De omleiding van de fout is gehandicapt (gebrek) wanneer dit het plaatsen of niet bepaald leeg is.

## PS::errorRedirect.connectTimeout - Redirect Connection Timeout {#section-3971be8f720d4b32a2cc7860b4085971}

Maximale tijd (in msec) waarop de server wacht tot een verbinding met de secundaire server tot stand is gebracht voordat een fout naar de client wordt geretourneerd.

## PS::errorRedirect.socketTimeout - Redirect Response Timeout {#section-69d8579f748d4044bca99dfb64dd523c}

Maximale tijd (in msec) de server zal op de secundaire server wachten om gegevens terug te keren alvorens het omleidingsverzoek te verlaten en een fout aan de cliënt terug te keren.
