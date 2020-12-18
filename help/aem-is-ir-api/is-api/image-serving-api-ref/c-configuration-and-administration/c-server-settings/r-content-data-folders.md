---
description: Gebruik deze serverinstellingen voor inhoudsgegevensmappen.
seo-description: Gebruik deze serverinstellingen voor inhoudsgegevensmappen.
seo-title: Inhoudsgegevensmappen
solution: Experience Manager
title: Inhoudsgegevensmappen
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Inhoudsgegevensmappen{#content-data-folders}

Gebruik deze serverinstellingen voor inhoudsgegevensmappen.

## IS::RootPath - Hoofdmappen voor afbeeldingsgegevens {#section-5c57569514bb4d00b19de31d2e137e3b}

De locatie van alle brongegevens, inclusief afbeeldingen, lettertypen en ICC-profielen. Dit kunnen een of meer absolute bestandspaden of paden zijn ten opzichte van *[!DNL install_folder]*, gescheiden met puntkomma&#39;s. Indien leeg, *[!DNL install_folder]* is de standaardwortel. U kunt meerdere waarden opgeven om afbeeldingsgegevens over meerdere bestandssystemen te verspreiden. De server van het Beeld zal de wortelwegen in de gespecificeerde orde proberen tot het gevraagde dossier wordt gevonden.

## PS::staticContent.rootPath - Static Content Data Root Folders {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

De locatie van statische inhoudsbrongegevens die via de context [!DNL /is/static] moeten worden geleverd. Kan een of meer absolute bestandspaden of paden zijn ten opzichte van *[!DNL install_folder]*, gescheiden met puntkomma&#39;s. Indien leeg, *[!DNL install_folder]* is de standaardwortel.

Meerdere waarden kunnen worden opgegeven, gescheiden door puntkomma&#39;s, om statische inhoud over meerdere bestandssystemen te distribueren. Wordt meestal ingesteld op dezelfde waarden als `IS::RootPath`.

De server van het Platform probeert de wortelwegen in de gespecificeerde orde tot het gevraagde dossier wordt gevonden.

>[!NOTE]
>
>Standaard wordt dit veld opzettelijk ingesteld op een niet-bestaande locatie ( [!DNL *[!DNL install_folder]*/static]), waardoor de service voor statische inhoud feitelijk wordt uitgeschakeld.

## IS::SaveDirectory - Bestandsopslaghoofdmap {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Het hoofdpad voor `attribute::SavePath` (wordt gebruikt door `req=saveToFile`). De server van het Beeld moet toegangstoestemmingen voor subfolder tot stand brengen waarin het beelddossiers zal creëren.
