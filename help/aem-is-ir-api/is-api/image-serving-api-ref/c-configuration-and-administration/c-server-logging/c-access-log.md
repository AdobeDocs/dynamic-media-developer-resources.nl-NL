---
description: Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.
seo-description: Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.
seo-title: Toegangslogboek
solution: Experience Manager
title: Toegangslogboek
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Toegangslogbestand{#access-log}

Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.

Het toegangslogboek wordt gevormd in server.xml.

>[!NOTE]
>
>Naast het clientverkeer voor Image Serving ( [!DNL /is/image/*]) en Image Rendering ( [!DNL /ir/render/*]), bevat het toegangslogboek mogelijk een bepaald intern verkeer: toegang tot het catalogussysteem van de Server van het Platform ( [!DNL /is-catalog/*]), geheime voorgeheugenverdeling en fout omleidingsverzoeken ( [!DNL /is/cache/*]), toegang tot andere pakketten die aan de Server van het Platform worden opgesteld, zoals de Kijkers van Dynamic Media ( [!DNL /is-viewers/*]), statische verkeer en statische inhoudverzoeken die door de Server van het Platform worden onderhouden (b.v. [!DNL /is-docs/*]).

Aanvragen met [!DNL /is-catalog] en [!DNL /is/cache] hoofdpaden moeten altijd worden uitgesloten van elke analyse van het clientverkeer.
