---
description: De configuratie-instellingen voor het renderen van afbeeldingen worden opgeslagen in het dialoogvenster [!DNL Platform Server] configuratiebestand.
solution: Experience Manager
title: Configuratiebestanden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Configuratiebestanden{#configuration-files}

De configuratie-instellingen voor het renderen van afbeeldingen worden opgeslagen in het dialoogvenster [!DNL Platform Server] configuratiebestand.

Het configuratiebestand van de platformserver bevindt zich op [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Dit bestand is een JAVA-eigenschappenbestand. Er moet op worden toegezien dat de desbetreffende conventies worden nageleefd, anders moet [!DNL Platform Server] kan niet beginnen. Een dubbele backslash (`\\`) of een enkele slash (/) moet worden gebruikt in plaats van een eenvoudige backslash (\) in Windows-bestandspaden, omdat de backslash wordt gebruikt als escape-teken in dit type bestand. Het bestand bevat niet-gedocumenteerde eigenschappen die voor intern servergebruik zijn en niet mogen worden gewijzigd.

Zie de [Referentie voor configuratie-instellingen](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) voor een lijst met alle configuratie-instellingen voor het renderen van afbeeldingen.
