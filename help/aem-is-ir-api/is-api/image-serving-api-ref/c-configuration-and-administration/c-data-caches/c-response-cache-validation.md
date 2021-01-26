---
description: De ingangen van het geheime voorgeheugen worden automatisch verfrist gebruikend of op catalogus-gebaseerde of op afloop-gebaseerde geheim voorgeheugenbevestiging, zoals geselecteerd met attribuut CacheValidationPolicy (in default.ini of het .ini dossier van een specifieke beeldcatalogus).
seo-description: De ingangen van het geheime voorgeheugen worden automatisch verfrist gebruikend of op catalogus-gebaseerde of op afloop-gebaseerde geheim voorgeheugenbevestiging, zoals geselecteerd met attribuut CacheValidationPolicy (in default.ini of het .ini dossier van een specifieke beeldcatalogus).
seo-title: Validatie van responscache
solution: Experience Manager
title: Validatie van responscache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Validatie van de responscache{#response-cache-validation}

Cachingangen worden automatisch vernieuwd met behulp van op een catalogus gebaseerde of op een vervaldatum gebaseerde cachevalidatie, zoals geselecteerd met kenmerk::CacheValidationPolicy (in default.ini of het .ini-bestand van een specifieke afbeeldingscatalogus).

Bij validatie op basis van een catalogus wordt een bestaand cacheitem als &#39;stable&#39; beschouwd als `catalog::LastModified` (of `attribute::LastModified`, of de tijd van de bestandswijziging van het [!DNL catalog.ini]-bestand) recenter is dan de tijd dat het cacheitem werd gemaakt.

Bij validatie op basis van vervaldatum wordt een cacheitem na 5 minuten sinds de meest recente validatie standaard verouderd. In beide gevallen valideert de server de items in de oude cache door de bestandsdatums te controleren van alle afbeeldingsbestanden die bij het maken van de aanvraag betrokken waren. Als de bestandsdatums niet zijn gewijzigd, wordt het tijdstempel van het cacheitem bijgewerkt en wordt de datum in de cache als geldig beschouwd.

Voor gangbare toepassingen waarbij vooral afbeeldingen in afbeeldingscatalogi worden opgenomen, biedt validatie op basis van catalogus een prestatievoordeel. Toepassingen die geen afbeeldingscatalogi bevatten, moeten op vervaldatum gebaseerde cachevalidatie gebruiken. U kunt dit bereiken door `attribute::cacheValidationPolicy=0` in [!DNL default.ini] en `1` in alle specifieke afbeeldingscatalogusbestanden in te stellen.

De ingangen van het geheime voorgeheugen worden ongeldig en zijn onderworpen aan re-generatie wanneer een catalogusingang betrokken bij het verzoek op een manier verandert die waarschijnlijk een verandering van het antwoordbeeld zou veroorzaken. De inhoud van `catalog::Modifier` verandert bijvoorbeeld.

>[!NOTE]
>
>In Dynamic Media piramid TIFF-afbeeldingen (PTIFF) wordt de bestandsdatum intern in de bestandsheader bewaard voor validatiedoeleinden. De wijzigingstijd van het bestand die door het bestandssysteem wordt aangehouden, wordt gebruikt om te controleren of een niet-PTIFF-bestand is gewijzigd.

Alleen afbeeldingsbestanden nemen deel aan het validatieproces van de cache. Wijzigingen in lettertypebestanden of ICC-profielbestanden leiden niet tot automatische ongeldigmaking van cachegegevens.
