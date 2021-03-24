---
description: Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.
solution: Experience Manager
title: Toegangslogboek
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Toegangslogbestand{#access-log}

Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.

Het toegangslogboek wordt gevormd in server.xml.

>[!NOTE]
>
>Naast het clientverkeer voor Image Serving ( [!DNL /is/image/*]) en Image Rendering ( [!DNL /ir/render/*]), bevat het toegangslogboek mogelijk een bepaald intern verkeer: toegang tot het catalogussysteem van de Server van het Platform ( [!DNL /is-catalog/*]), geheime voorgeheugenverdeling en fout omleidingsverzoeken ( [!DNL /is/cache/*]), toegang tot andere pakketten die aan de Server van het Platform worden opgesteld, zoals de Kijkers van Dynamic Media ( [!DNL /is-viewers/*]), statische verkeer en statische inhoudverzoeken die door de Server van het Platform worden onderhouden (b.v. [!DNL /is-docs/*]).

Aanvragen met [!DNL /is-catalog] en [!DNL /is/cache] hoofdpaden moeten altijd worden uitgesloten van elke analyse van het clientverkeer.
