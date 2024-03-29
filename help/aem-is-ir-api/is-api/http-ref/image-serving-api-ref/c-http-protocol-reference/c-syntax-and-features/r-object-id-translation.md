---
description: De Beeldserver biedt een mechanisme om externe objecten-id's te vertalen naar landspecifieke object-id's (catalogus). De primaire toepassing is het aanbieden van landspecifieke inhoud en inhoud die door meerdere landinstellingen wordt gedeeld, zonder dat de clienttoepassing de landspecifieke object-id's moet kennen.
solution: Experience Manager
title: Omzetten van object-id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# Omzetten van object-id{#object-id-translation}

De Beeldserver biedt een mechanisme om externe objecten-id&#39;s te vertalen naar landspecifieke object-id&#39;s (catalogus). De primaire toepassing is het aanbieden van landspecifieke inhoud en inhoud die door meerdere landinstellingen wordt gedeeld, zonder dat de clienttoepassing de landspecifieke object-id&#39;s moet kennen.

De toepassing kan alleen worden geschreven met behulp van algemene object-id&#39;s en Image Serving vervangt automatisch landspecifieke afbeeldingen en andere inhoud, indien beschikbaar.

De *`locale`* wordt opgegeven in aanvragen voor beeldverwerking bij de `locale=` gebruiken.

>[!NOTE]
>
>Vertalen van object-id is alleen van toepassing voor gebruik van afbeeldingsserver op basis van catalogus. Bestandsnamen kunnen niet worden vertaald.

## Toepassingsgebied {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Alle verwijzingen naar items in afbeeldings-, SVG- en statische inhoudcatalogi worden beschouwd als verwijzingen naar vertaallettertypen en ICC-profielverwijzingen worden niet vertaald. Naast de *`object`* in het pad van [!DNL /is/image] en [!DNL /is/static requests], zijn deze opdrachten en cataloguskenmerken onderhevig aan id-omzetting: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, en `attribute::Watermark`.

## De vertaalkaart voor id {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` bepaalt de regels die door de server worden gebruikt om identiteitskaart van de gelokaliseerde inhoud te bepalen, gegeven als input generische objecten identiteitskaart en `locale=` waarde.

`attribute::LocaleMap` bestaat uit een lijst van input *landinstellingen* (die overeenkomen met de waarden die zijn opgegeven met `locale=`), elk met geen of meer achtervoegsels van de uitvoerlandinstelling ( `*`locSuffixes`*`).

Bijvoorbeeld: `attribute::LocaleMap` kan er als volgt uitzien:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

Het verzoek `/is/image/myCat/myImg?locale=de_de` retourneert de afbeelding die aan het catalogusitem is gekoppeld `myCat/myImg_D` (ervan uitgaande dat een dergelijke vermelding in de catalogus bestaat).

Zie de beschrijving van `attribute::LocaleMap` voor meer informatie.

## Het vertaalproces {#section-1f64db17e9f644d88e09853670e14a16}

In het bovenstaande voorbeeld zoekt de server eerst naar de *`locale`* &quot; `de_de`&quot; in de vertaalkaart van identiteitskaart Vervolgens wordt er herhaald over de *`locSuffixes`* in dit geval&quot; `_D`&quot; en &quot;&quot; (leeg achtervoegsel). Voor elke herhaling wordt het achtervoegsel toegevoegd aan de afbeeldings-id en wordt de resulterende id getest op aanwezigheid in de catalogus. Indien gevonden, wordt dat catalogusitem gebruikt, anders wordt het volgende item getest. In dit voorbeeld worden de volgende items gecontroleerd: `myCat/myImg_D`, en `myCat/myImg`. Als geen gelijke wordt gevonden, keert de server een fout of een standaardbeeld (als zo gevormd) terug.

## Onbekende landinstellingen {#section-b2f3c83f2dc845d69b5908107b775537}

In het bovenstaande voorbeeld: `attribute::LocaleMap` bevat een lege *`locale`* waarmee de standaardvertaalregel wordt gedefinieerd die voor onbekend wordt gebruikt `locale=` waarden (dat wil zeggen waarden die niet expliciet in de vertaalkaart worden vermeld). Als deze vertaalkaart op de aanvraag is toegepast `/is/image/myCat/myImg?locale=ja`, wil zij `myCat/myImg_E`, indien deze bestaat, of anderszins `myCat/myImg`.

Als een vertaalkaart geen standaardvertaalregel specificeert, is een fout teruggekeerd voor alle verzoeken met onbekend `locale=` waarden.

## Voorbeelden {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Opzoeken op meerdere niveaus**

Het is vaak wenselijk om landinstellingen (bijvoorbeeld Europees, Midden-Oosten, Noord-Amerika) te groeperen om regionale normen aan te pakken. Dit kan met een multi-tiered raadpleging worden bereikt.

Voor dit voorbeeld willen we collecties voor gebruik in het Westen en het Midden-Oosten ondersteunen. Beide verzamelingen zijn gebaseerd op de algemene afbeeldingsverzameling en voegen of wijzigen enkele afbeeldingen toe. Beide verzamelingen worden vervolgens verder verfijnd voor specifieke landinstellingen ( `m1`, `m2` voor twee varianten in het midden-oosten, en `w1`, `w2`, en `w3` voor drie westerse landinstellingen), behalve dat afbeeldingen worden gedeeld voor `w1` en `w3`. Onbekende landinstellingen worden alleen toegewezen aan de algemene verzameling en hebben geen toegang tot landspecifieke afbeeldingen.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

In de volgende tabel wordt aangegeven welke catalogusitems in overweging worden genomen en in welke volgorde ze worden gebruikt voor de generieke invoer-id `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>landinstelling</i> </b> </th> 
   <th class="entry"> <b>Te doorzoeken catalogus-id's</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alle andere </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Zoeken naar specifieke id&#39;s**

Sommige naamgevingsconventies voor afbeeldingen bieden mogelijk geen interne ondersteuning voor algemene afbeeldings-id&#39;s. De generieke id&#39;s van het verzoek moeten altijd worden toegewezen aan een specifieke id in de catalogus. Het is vaak mogelijk dat de exacte specifieke id niet bekend is.

In dit voorbeeld kunnen afbeeldingen voor alle talen `_1`, `_2`, of `_3` achtervoegsel. Afbeeldingen die specifiek zijn voor Franse landinstellingen kunnen `_22` of `_23` achtervoegsel en afbeeldingen die specifiek zijn voor Duitse landinstellingen kunnen `_470` of `_480` achtervoegsel.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

In de volgende tabel wordt aangegeven welke catalogusitems in overweging worden genomen en in welke volgorde ze worden gebruikt voor de generieke invoer-id `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>landinstelling</i> </b> </th> 
   <th class="entry"> <b>Uitvoer-id's die moeten worden doorzocht</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alle andere </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zie ook {#section-05893816c66a406d89f9bfd6ace8d47a}

[kenmerk:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [kenmerk::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
