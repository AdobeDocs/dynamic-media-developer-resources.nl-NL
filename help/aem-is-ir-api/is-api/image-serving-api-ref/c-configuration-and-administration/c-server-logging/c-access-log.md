---
description: Dit is het primaire logboek dat spoor houdt van alle HTTP- verzoeken die aan [!DNL Platform Server]. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.
solution: Experience Manager
title: Toegangslogboek
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Toegangslogboek{#access-log}

Dit is het primaire logboek dat spoor houdt van alle HTTP- verzoeken die aan [!DNL Platform Server]. Als de functie Afbeelding renderen is ingeschakeld, worden de gegevens in het toegangslogboek naar hetzelfde bestand geschreven.

Het toegangslogboek wordt gevormd in server.xml.

>[!NOTE]
>
>Naast cliëntverkeer voor Beeld Serving ( [!DNL /is/image/*]) en afbeeldingen renderen ( [!DNL /ir/render/*]), kan het toegangslogboek bepaalde interne verkeer omvatten: toegang tot de [!DNL Platform Server] catalogussysteem ( [!DNL /is-catalog/*]), cache delen en aanvragen voor omleiding van fouten ( [!DNL /is/cache/*]), toegang tot andere pakketten die worden ingezet in de [!DNL Platform Server], zoals Dynamic Media Viewers ( [!DNL /is-viewers/*]), statische verkeer en statische inhoudverzoeken die door [!DNL Platform Server] (bijvoorbeeld [!DNL /is-docs/*]).

Verzoeken met [!DNL /is-catalog] en [!DNL /is/cache] de wortelwegen zouden altijd van om het even welke analyse van het cliëntverkeer moeten worden uitgesloten.
