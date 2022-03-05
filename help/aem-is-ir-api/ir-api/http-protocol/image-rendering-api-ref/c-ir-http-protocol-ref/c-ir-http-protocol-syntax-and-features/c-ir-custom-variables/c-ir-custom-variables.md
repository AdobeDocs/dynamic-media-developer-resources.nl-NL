---
title: Aangepaste variabelen
description: Het vraaggedeelte van verzoeken en de koorden van de Modifier van het vignet kunnen user-defined variabelen omvatten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Aangepaste variabelen{#custom-variables}

Het querygedeelte van aanvragen en vignet::Modifier-tekenreeksen kunnen door de gebruiker gedefinieerde variabelen bevatten.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Naam variabele. Kan bestaan uit elke combinatie van alfa-, cijfer- en veilige tekens, met uitzondering van `$`.

`[!DNL value]` - Waarde waarop de variabele moet worden ingesteld (tekenreeks).

Variabelen worden op dezelfde manier gedefinieerd als andere serveropdrachten, met behulp van de bovenstaande syntaxis. Variabelen moeten worden gedefinieerd voordat naar deze variabelen kan worden verwezen. Variabelen die worden gedefinieerd in `vignette::Modifier` kan in het URL verzoek worden van verwijzingen voorzien, en omgekeerd.

>[!NOTE]
>
>`[!DNL value]` moet URL-gecodeerd voor één controle zijn voor veilige HTTP-verzending. Dubbele codering is vereist als `[!DNL value]` wordt opnieuw verzonden via HTTP. Dit is het geval wanneer `[!DNL value]` wordt vervangen door een geneste externe aanvraag.

Er wordt verwezen naar variabelen door de naam van de variabele in te sluiten (ingesloten door een regelafstand en een volgteken) `$`) ergens in opdrachtwaarden. Bijvoorbeeld tussen `=`  na de opdrachtnaam en de volgende `&` of het einde van het verzoek. De server vervangt elk exemplaar van `$ [!DNL name]$` with `[!DNL string]`. Er vinden geen substituties plaats op elk moment van `$ [!DNL name]$` in bevelnamen (vóór het gelijke teken van een bevel), en in het weggedeelte van het verzoek.

Aangepaste variabelen kunnen niet worden genest. Alle exemplaren van `$ [!DNL name]$` binnen `[!DNL string]` niet vervangen. Het aanvraagfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` lost aan `text=my$var2$tree`.

`$` geen gereserveerd teken is; het kan anders in het verzoek voorkomen. Bijvoorbeeld: `src=my$texture$file.tif` is een geldige opdracht (er wordt van uitgegaan dat een item of structuurbestand met de naam van een materiaalcatalogus `[!DNL my$texture$file.tif]` bestaat), while `wid=$number$` is niet, omdat `wid=` vereist een numeriek argument.
