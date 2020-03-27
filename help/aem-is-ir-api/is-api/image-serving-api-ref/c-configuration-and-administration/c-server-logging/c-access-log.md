---
description: Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.
seo-description: Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.
seo-title: Toegangslogboek
solution: Experience Manager
title: Toegangslogboek
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Toegangslogboek{#access-log}

Dit is het primaire logboek dat spoor van alle HTTP- verzoeken bijhoudt die aan de Server van het Platform worden gemaakt. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.

Het toegangslogboek wordt gevormd in server.xml.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Naast cliëntverkeer voor het Beeld Serven ( [!DNL /is/image/*]) en Beeld Renderen ( [!DNL /ir/render/*]), kan het toegangslogboek bepaald intern verkeer omvatten: toegang tot het de catalogussysteem van de Server van het Platform ( [!DNL /is-catalog/*]), geheime voorgeheugen het delen en fout richten verzoeken ( [!DNL /is/cache/*]), toegang tot andere pakketten die aan de Server van het Platform worden opgesteld, zoals de Kijkers Scene7 ( [!DNL /is-viewers/*]), statische verkeer en statische inhoudsverzoeken die door de Server van het Platform worden onderhouden (b.v. [!DNL /is-docs/*]).

Verzoeken met [!DNL /is-catalog] en [!DNL /is/cache] hoofdpaden moeten altijd worden uitgesloten van iedere analyse van het clientverkeer.
