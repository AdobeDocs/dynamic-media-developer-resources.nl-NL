---
description: Het vraaggedeelte van verzoeken en de koorden van de Modifier van het vignet kunnen user-defined variabelen omvatten.
seo-description: Het vraaggedeelte van verzoeken en de koorden van de Modifier van het vignet kunnen user-defined variabelen omvatten.
seo-title: Aangepaste variabelen
solution: Experience Manager
title: Aangepaste variabelen
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Aangepaste variabelen{#custom-variables}

Het querygedeelte van aanvragen en vignet::Modifier-tekenreeksen kunnen door de gebruiker gedefinieerde variabelen bevatten.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Naam variabele. Kan bestaan uit een willekeurige combinatie van alfa-, cijfer- en veilige tekens, met uitzondering van &#39;$.&#39;

** *[!DNL value]* * Waarde waarop de variabele moet worden ingesteld (tekenreeks).

Variabelen worden op dezelfde manier gedefinieerd als andere serveropdrachten, met behulp van de bovenstaande syntaxis. Variabelen moeten worden gedefinieerd voordat naar deze variabelen kan worden verwezen. Variabelen die in worden gedefinieerd, `vignette::Modifier` kunnen worden vermeld in de URL-aanvraag en andersom.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>*[!DNL value]* moet URL-gecodeerd voor één controle zijn voor veilige HTTP-verzending. Dubbele codering is vereist als de gegevens opnieuw via HTTP *[!DNL value]* worden verzonden. Dit is het geval wanneer *[!DNL value]* wordt vervangen in een geneste buitenlandse aanvraag.

Er wordt verwezen naar variabelen door de variabelenaam (ingesloten door een regelafstand en een navolgende $) ergens in opdrachtwaarden in te sluiten. Bijvoorbeeld tussen &#39;=&#39; volgend op de opdrachtnaam en de volgende &#39;&amp;&#39; of het einde van de aanvraag. Elk exemplaar van $ *[!DNL name]*$ wordt door de server vervangen *[!DNL string]*. Er vindt geen vervanging plaats bij elke instantie van $ *[!DNL name]*$ in opdrachtnamen (vóór het gelijkteken van een opdracht) en in het padgedeelte van de aanvraag.

Aangepaste variabelen kunnen niet worden genest. Voorvallen van $ *[!DNL name]*$ binnen *[!DNL string]* worden niet vervangen. Het aanvraagfragment wordt bijvoorbeeld `$var2=apple&$var1=my$var2$tree&text=$var1$` omgezet in `text=my$var2$tree`.

$ is geen gereserveerd teken; het kan anders in het verzoek voorkomen. Dit `src=my$texture$file.tif` is bijvoorbeeld een geldige opdracht (er wordt van uitgegaan dat een item of structuurbestand met de naam van een materiaalcatalogus [!DNL my$texture$file.tif] bestaat), `wid=$number$` maar niet, omdat een numeriek argument `wid=` vereist is.
