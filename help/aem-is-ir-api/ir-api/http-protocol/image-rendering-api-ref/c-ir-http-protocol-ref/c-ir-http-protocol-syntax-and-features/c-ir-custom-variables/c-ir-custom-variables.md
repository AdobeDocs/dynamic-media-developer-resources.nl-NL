---
description: Het vraaggedeelte van verzoeken en de koorden van de Modifier van het vignet kunnen user-defined variabelen omvatten.
seo-description: Het vraaggedeelte van verzoeken en de koorden van de Modifier van het vignet kunnen user-defined variabelen omvatten.
seo-title: Aangepaste variabelen
solution: Experience Manager
title: Aangepaste variabelen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Aangepaste variabelen{#custom-variables}

Het querygedeelte van aanvragen en vignet::Modifier-tekenreeksen kunnen door de gebruiker gedefinieerde variabelen bevatten.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Naam variabele. Kan bestaan uit een willekeurige combinatie van alfa-, cijfer- en veilige tekens, met uitzondering van &#39;$.&#39;

** *[!DNL value]* * Waarde waarop de variabele moet worden ingesteld (tekenreeks).

Variabelen worden op dezelfde manier gedefinieerd als andere serveropdrachten, met behulp van de bovenstaande syntaxis. Variabelen moeten worden gedefinieerd voordat naar deze variabelen kan worden verwezen. Variabelen die zijn gedefinieerd in `vignette::Modifier`, kunnen worden vermeld in het URL-verzoek en andersom.

>[!NOTE]
>
>*[!DNL value]* moet URL-gecodeerd voor één controle zijn voor veilige HTTP-verzending. Dubbele codering is vereist als *[!DNL value]* opnieuw wordt verzonden via HTTP. Dit is het geval wanneer *[!DNL value]* in een genesteld buitenlands verzoek wordt vervangen.

Er wordt verwezen naar variabelen door de variabelenaam (ingesloten door een regelafstand en een navolgende $) ergens in opdrachtwaarden in te sluiten. Bijvoorbeeld tussen &#39;=&#39; volgend op de opdrachtnaam en de volgende &#39;&amp;&#39; of het einde van de aanvraag. De server vervangt elk exemplaar van $ *[!DNL name]*$ door *[!DNL string]*. Er vinden geen substituties plaats op elk exemplaar van $ *[!DNL name]*$ in opdrachtnamen (vóór het gelijkteken van een opdracht) en in het padgedeelte van het verzoek.

Aangepaste variabelen kunnen niet worden genest. Voorvallen van $ *[!DNL name]*$ binnen *[!DNL string]* worden niet vervangen. Het aanvraagfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` wordt bijvoorbeeld omgezet in `text=my$var2$tree`.

$ is geen gereserveerd teken; het kan anders in het verzoek voorkomen. `src=my$texture$file.tif` is bijvoorbeeld een geldige opdracht (ervan uitgaande dat een item in de materiaalcatalogus of een structuurbestand met de naam [!DNL my$texture$file.tif] bestaat), terwijl `wid=$number$` dat niet is, omdat `wid=` een numeriek argument vereist.
