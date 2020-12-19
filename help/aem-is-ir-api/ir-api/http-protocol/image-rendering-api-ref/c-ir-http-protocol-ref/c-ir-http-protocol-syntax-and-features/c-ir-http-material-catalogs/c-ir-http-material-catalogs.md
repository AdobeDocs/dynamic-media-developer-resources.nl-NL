---
description: Materiaalcatalogi bieden verschillende functies.
seo-description: Materiaalcatalogi bieden verschillende functies.
seo-title: Materiaalcatalogi *
solution: Experience Manager
title: Materiaalcatalogi *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Materiaalcatalogi *{#material-catalogs}

Materiaalcatalogi bieden verschillende functies.

* Persistente definitie van materialen toestaan, inclusief alle materiaaleigenschappen.

   Naar materialen die zijn gedefinieerd in de materiaalcatalogus kan worden verwezen met een eenvoudige id in plaats van met een reeks eigenschappen van materiaal.
* Geef standaardwaarden op voor bepaalde aanvraagkenmerken, zoals de JPEG-kwaliteit of een standaardgrootte voor de antwoordafbeelding.
* U kunt vignetten, ICC-profielen en aanvraagsjablonen beheren.

Zelfs als er geen specifieke materiaalcatalogi zijn gedefinieerd, zijn alle functies van materiaalcatalogi beschikbaar via de standaardcatalogus ( [!DNL default.ini]).

Hoewel rendermaterialen expliciet kunnen worden opgegeven in aanvragen waarbij gebruik wordt gemaakt van materiaalkenmerken, is het in veel gevallen beter om de details van materialen van de website te verbergen met behulp van materiaalcatalogi. src= - opdrachten accepteren catalogusverwijzingen in plaats van expliciete bestandspaden. Een catalogusitem bestaat uit ` [ *[!DNL catId]*/] *[!DNL itemId]*`, waarbij ` *[!DNL catId]*` een materiaalcatalogus identificeert en ` *[!DNL itemId]*` een record in de catalogus identificeert. Als ` *[!DNL catId]*` niet wordt gespecificeerd, wordt de zittingscatalogus gebruikt (zie hieronder).

Een catalogusrecord wordt gevonden als (a) ` *[!DNL catId]*` overeenkomt met de `attribute::RootId`-waarde van een materiaalcatalogus en (b) ` *[!DNL recId]*` overeenkomt met de catalogus::Id-waarde in dezelfde catalogus. In het geval van een geslaagde overeenkomst worden de kenmerken van het materiaal (inclusief `src=`) ingesteld op de gegevens uit de catalogusrecord. Als het MSS extra attributen voor dit materiaal behalve src= omvat, treden zij de waarden van het catalogusverslag met voeten.

Als ` *[!DNL recId]*` niet aan een catalogusingang kan worden aangepast, dan ` *[!DNL catId]*` wordt vervangen met `attribute::RootPath` van de catalogus en de resulterende weg wordt dan verondersteld om een eenvoudig dossierweg te zijn. Andere standaardkenmerken (bv. `attribute::Resolution`) kan ook van de materiaalcatalogus worden geërft.

Vignetten en ICC-profielen kunnen worden gespecificeerd in materiaalcatalogi die lijken op de materialen zelf en in bepaalde eigenschappen. Bovendien biedt de vignetkaart ook de container voor sjablonen.

**Zie ook**

Referentie materiaalcatalogus, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
