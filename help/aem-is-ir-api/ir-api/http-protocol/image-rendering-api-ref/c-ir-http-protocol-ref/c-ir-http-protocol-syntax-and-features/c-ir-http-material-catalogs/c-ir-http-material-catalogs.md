---
title: Materiaalcatalogi
description: Materiaalcatalogi bieden verschillende functies.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Materiaalcatalogi {#material-catalogs}

Materiaalcatalogi bieden verschillende functies.

* Persistente definitie van materialen toestaan, inclusief alle materiaaleigenschappen.

  Naar materialen die zijn gedefinieerd in de materiaalcatalogus kan worden verwezen met een eenvoudige id in plaats van met een reeks eigenschappen van materiaal.
* Geef standaardwaarden op voor bepaalde aanvraagkenmerken, zoals de kwaliteit van de JPEG of de grootte van een standaardantwoordafbeelding.
* U kunt vignetten, ICC-profielen en aanvraagsjablonen beheren.

Zelfs als er geen specifieke materiaalcatalogi zijn gedefinieerd, zijn alle functies van materiaalcatalogi beschikbaar in de standaardcatalogus ( [!DNL default.ini]).

Hoewel rendermaterialen expliciet kunnen worden opgegeven in aanvragen met materiaalkenmerken, is het vaak beter om de details van materialen van de website te verbergen met behulp van materiaalcatalogi. src= - opdrachten accepteren catalogusverwijzingen in plaats van expliciete bestandspaden. Een item in een catalogus bestaat uit ` [ *[!DNL catId]*/] *[!DNL itemId]*`, waarbij ` *[!DNL catId]*` een materiële catalogus identificeert en ` *[!DNL itemId]*` Hiermee wordt een record in de catalogus aangegeven. Indien ` *[!DNL catId]*` niet is opgegeven, wordt de sessiecatalogus gebruikt (zie hieronder).

Een catalogusrecord wordt gevonden als (a) ` *[!DNL catId]*` komt overeen met de `attribute::RootId` de waarde van een materiaalcatalogus en b) ` *[!DNL recId]*` komt overeen met de catalogus::Id-waarde in dezelfde catalogus. Als er een overeenkomst is, worden de kenmerken van het materiaal (inclusief `src=`) worden ingesteld op de gegevens uit de catalogusrecord. Als het MSS extra attributen voor dit materiaal behalve src= omvat, treden zij de waarden van het catalogusverslag met voeten.

Indien ` *[!DNL recId]*` kan niet worden gekoppeld aan een item in een catalogus, en ` *[!DNL catId]*` wordt vervangen door `attribute::RootPath` in de catalogus en het resulterende pad wordt dan als een eenvoudig bestandspad beschouwd. Andere standaardkenmerken (bijvoorbeeld `attribute::Resolution`) kan ook van de materiaalcatalogus worden overgeërfd.

Vignetten en ICC-profielen kunnen worden gespecificeerd in materiaalcatalogi die lijken op de materialen zelf en in bepaalde eigenschappen. Bovendien biedt de vignetkaart ook de container voor sjablonen.

**Zie ook**

Referentie materiaalcatalogus; [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
