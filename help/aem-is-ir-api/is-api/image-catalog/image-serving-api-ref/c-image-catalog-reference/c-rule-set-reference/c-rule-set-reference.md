---
description: De Server van het beeld steunt een eenvoudig verzoek preprocessing mechanisme dat op regelmatige-uitdrukkingsgelijke en substitutieregels gebaseerd is.
seo-description: De Server van het beeld steunt een eenvoudig verzoek preprocessing mechanisme dat op regelmatige-uitdrukkingsgelijke en substitutieregels gebaseerd is.
seo-title: Referentie voor regelset
solution: Experience Manager
title: Referentie voor regelset
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Referentie voor regelset{#rule-set-reference}

De Server van het beeld steunt een eenvoudig verzoek preprocessing mechanisme dat op regelmatige-uitdrukkingsgelijke en substitutieregels gebaseerd is.

Verzamelingen van voorverwerkingsregels (*regelsets*) kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus. De regels in de standaardcatalogus zijn alleen van toepassing als in de aanvraag geen specifieke hoofdafbeeldingscatalogus wordt geïdentificeerd.

De pre-verwerkingsregels van het verzoek kunnen de weg en vraaggedeelten verzoeken wijzigen alvorens zij door de parser van de Server van het Platform, met inbegrip van het manipuleren van de weg, het toevoegen van bevelen, het veranderen van bevelwaarden, en het toepassen van malplaatjes of macro&#39;s worden verwerkt. De regels kunnen ook worden gebruikt om bepaalde veiligheidseigenschappen te vormen en met voeten te treden die normaal slechts met catalogusattributen, zoals verzoekverwarring, water-markering, en het beperken van de dienst tot specifieke cliëntIP adressen worden gecontroleerd.

Regelsets worden opgeslagen als XML-documentbestanden. Het relatieve of absolute pad van het bestand met regelsets moet worden opgegeven in `attribute::RuleSetFile`.

## Algemene structuur {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

De `<?xml>` en `<ruleset>` elementen zijn altijd vereist in een geldig XML-bestand met regelsets, zelfs als er geen werkelijke regels zijn gedefinieerd.

Eén `<ruleset>` element met een willekeurig aantal `<rule>` elementen is toegestaan.

De inhoud van regelbestanden voor voorbewerken is hoofdlettergevoelig.

## Validatie van regels {#section-d8d101a0b4d74580835e37d128d05567}

Er [!DNL RuleSet.xsd] is een kopie van deze code beschikbaar in de catalogusmap en deze moet worden gebruikt om een bestand met regels te valideren voordat het in het [!DNL catalog.ini] bestand wordt geregistreerd. Merk op dat de Serving van het Beeld een interne exemplaar van [!DNL RuleSet.xsd] voor bevestiging gebruikt.

## URL-voorbewerking {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Voordat een nieuwe verwerking wordt uitgevoerd, wordt een inkomende HTTP-aanvraag gedeeltelijk geparseerd om te bepalen welke afbeeldingscatalogus moet worden toegepast. Nadat de catalogus is geïdentificeerd, wordt de regelset toegepast voor de geselecteerde catalogus (of de standaardcatalogus als er geen specifieke catalogus is geïdentificeerd).

De `<rule>` elementen worden gezocht in de orde die voor een gelijke met de inhoud van het `<expression>` element ( *`expression`*) wordt gespecificeerd.

Als een `<rule>` gelijke, facultatief *`substitution`* wordt toegepast en het gewijzigde verzoekkoord wordt overgegaan tot de verzoekparser van de server voor normale verwerking.

Als geen succesvolle gelijke wordt gemaakt wanneer het eind van het `<ruleset>` wordt bereikt, wordt het verzoek overgegaan tot parser zonder wijziging.

## Het kenmerk OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Het standaardgedrag kan met het `OnMatch` attribuut van het `<rule>` element worden gewijzigd. `OnMatch` kan worden ingesteld op `break` (standaardwaarde), `continue`of `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Element en kenmerk</b> </th> 
   <th class="entry"> <b>Gedrag wanneer een overeenkomst plaatsvindt</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>Regelverwerking wordt onmiddellijk beëindigd nadat de vervanging van deze regel is toegepast. Standaard. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>De vervanging wordt toegepast en de verwerking gaat verder met de volgende regel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>Regelverwerking wordt onmiddellijk beëindigd en een "verzoek geweigerd"antwoordstatus wordt teruggegeven aan de cliënt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cataloguskenmerken overschrijven {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` elementen kunnen desgewenst kenmerken definiëren die de overeenkomende cataloguskenmerken overschrijven wanneer de regel correct wordt aangepast. Als meerdere overeenkomende regels hetzelfde kenmerk instellen, heeft de laatste voorrang. Raadpleeg de beschrijving van het ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` element voor een lijst met kenmerken die met regels kunnen worden beheerd.

## Reguliere expressies {#section-3f77bb9a265147b38c645f63ab1bad8b}

Eenvoudige tekenreeksovereenkomsten werken voor zeer eenvoudige toepassingen, maar in de meeste gevallen zijn reguliere expressies vereist. Reguliere expressies zijn industriestandaard, maar de specifieke implementatie verschilt per geval.

[ [!DNL-pakket java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschrijft de specifieke standaardimplementatie voor expressies die door Image Serving wordt gebruikt.

## Vastgelegde subtekenreeksen {#section-066e659406d5403599cd26ae35e80d68}

Om complexe URL-wijzigingen mogelijk te maken, kunnen subtekenreeksen worden vastgelegd in de expressie door de subtekenreeks tussen haakjes (...) te plaatsen. Vastgelegde subtekenreeksen worden opeenvolgend genummerd, beginnend met 1 op basis van de positie van het voorloophaakje. De vastgelegde subtekenreeksen kunnen in de vervanging worden ingevoegd met ` $ *`n`*`, waarbij *`n`* het volgnummer van de vastgelegde subtekenreeks is.

## Bestanden met regelsets beheren {#section-0598a608e4044bb4805fe93ceebe10a9}

Met het kenmerk Catalog kunt u één bestand met een regelset koppelen aan elke afbeeldingscatalogus `attribute::RuleSetFile`. U kunt het regelsetbestand op elk gewenst moment bewerken, maar de afbeeldingsserver herkent de wijzigingen alleen wanneer de bijbehorende afbeeldingscatalogus opnieuw wordt geladen. Dit wordt opnieuw geladen wanneer de platformserver wordt gestart of opnieuw wordt gestart en wanneer het primaire catalogusbestand met het achtervoegsel [!DNL .ini] bestand wordt gewijzigd of &quot;aangeraakt&quot; om de bestandsdatum te wijzigen.

## Voorbeelden {#section-aa769437d967459299b83a4bf34fe924}

**Voorbeeld A.** Definieer een regel die de afbeeldingskwaliteitsinstellingen verhoogt als de afbeeldingsnaam het achtervoegsel &quot; [!DNL _hg]&quot; heeft:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

Met de regelexpressie wordt een niet-hoofdlettergevoelige overeenkomst van &quot; [!DNL _hg]&quot; opgegeven aan het einde van de URL-tekenreeks. Het achtervoegsel wordt vervangen door de opgegeven queryreeks waarmee de afbeeldingskwaliteitsinstellingen worden gewijzigd. Het `?` teken in de vervangende tekenreeks wordt genegeerd, omdat dit een speciaal teken in reguliere expressies is.

>[!NOTE]
>
>De vereiste codering voor het ampersand-teken. U kunt de vervangende tekenreeks ook insluiten in een CDATA-blok:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Voorbeeld B.** Een bepaalde webtoepassing staat geen querytekenreeksen toe. Definieer een regel die het navolgende padelement vertaalt `small`, `medium`of `large` naar een sjabloon, waarbij de rest van het pad als afbeeldingsnaam wordt gebruikt. Bijvoorbeeld, zou `myCat/myImage/small` vertalen naar `myCat/smallTemplate?src=myCat/myImage`.

U kunt subtekenreeksen gebruiken om de aanvraag te herstructureren:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Zie ook {#section-9b748e7c5cff4759a70f96657bd43352}

[pakket java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
