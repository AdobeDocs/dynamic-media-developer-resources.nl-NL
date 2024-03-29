---
description: Rendering van afbeeldingen ondersteunt een eenvoudig voorbewerkingsmechanisme voor aanvragen dat is gebaseerd op regels voor het afstemmen van reguliere expressies en het vervangen van expressies.
solution: Experience Manager
title: Referentie voor regelset
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Referentie voor regelset{#rule-set-reference}

Rendering van afbeeldingen ondersteunt een eenvoudig voorbewerkingsmechanisme voor aanvragen dat is gebaseerd op regels voor het afstemmen van reguliere expressies en het vervangen van expressies.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Verzamelingen van voorverwerkingsvoorschriften (*regelsets*) kan aan materiaalcatalogi of de standaardcatalogus worden toegevoegd. De regels in de standaardcatalogus zijn alleen van toepassing als de aanvraag geen specifieke materiaalcatalogus bevat.

De pre-verwerkingsregels van het verzoek kunnen de weg en vraaggedeelten verzoeken wijzigen alvorens zij door de verzoekparser van de server, met inbegrip van het manipuleren van de weg, het toevoegen van bevelen, het veranderen van bevelwaarden, en het toepassen van malplaatjes of macro&#39;s worden verwerkt. De regels kunnen ook worden gebruikt om sommige catalogusattributen te vormen en met voeten te treden, evenals voor het beperken van de dienst tot specifieke cliëntIP adressen.

Regelsets worden opgeslagen als XML-documentbestanden. Het relatieve of absolute pad van het bestand met regelsets moet worden opgegeven in `attribute::RuleSetFile`.

## Algemene structuur {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

De `<?xml>`, `<!DOCTYPE>` en `<ruleset>` elementen zijn altijd vereist in een geldig XML-bestand met regelsets, zelfs als er geen werkelijke regels zijn gedefinieerd.

Eén `<ruleset>` element met een willekeurig aantal elementen `<rule>` elementen zijn toegestaan.

De inhoud van het voorbewerken van regelbestanden is hoofdlettergevoelig.

## URL-voorbewerking {#section-737a38d1b8c746f995e64fa6cfbcec87}

Vóór een andere verwerking, wordt een inkomende HTTP- verzoek gedeeltelijk ontleed om te bepalen welke materiaalcatalogus zou moeten worden toegepast. Nadat de catalogus is geïdentificeerd, wordt de regelset toegepast voor de geselecteerde catalogus (of de standaardcatalogus als er geen specifieke catalogus is geïdentificeerd).

De `<rule>` elementen worden gezocht in de orde die voor de inhoud van wordt gespecificeerd `<expression>` element ( *`expression`*).

Indien een `<rule>` komt overeen met de optionele *`substitution`* wordt toegepast en het gewijzigde verzoekkoord wordt overgegaan tot de verzoekparser van de server voor normale verwerking.

Als er geen overeenkomende waarde is gevonden aan het einde van de `<ruleset>` wordt bereikt, wordt het verzoek ongewijzigd aan de parser overgegaan.

## Het kenmerk OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Het standaardgedrag kan worden gewijzigd met de `OnMatch` kenmerk van de `<rule>` elementen. `OnMatch` kan worden ingesteld op `break` (standaard), `continue`, of `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element en kenmerk </p> </th> 
   <th colname="col2" class="entry"> <p>Gedrag wanneer een overeenkomst plaatsvindt </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Regelverwerking wordt onmiddellijk beëindigd nadat de vervanging van deze regel is toegepast. Standaard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>De vervanging wordt toegepast en de verwerking gaat verder met de volgende regel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Regelverwerking wordt onmiddellijk beëindigd en een "verzoek geweigerd"antwoordstatus wordt teruggegeven aan de cliënt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cataloguskenmerken overschrijven {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` elementen kunnen desgewenst kenmerken definiëren die de overeenkomende cataloguskenmerken overschrijven wanneer de regel is aangepast en `OnMatch="break"` is ingesteld. Er worden geen kenmerken toegepast als `OnMatch="continue"` is ingesteld. Zie de beschrijving van `<rule>` voor een lijst van attributen die met regels kunnen worden gecontroleerd.

## Reguliere expressies {#section-4d326507b52544b0960a9a5f303e3fe6}

Eenvoudige tekenreeksovereenkomsten werken voor zeer eenvoudige toepassingen, maar in de meeste gevallen zijn reguliere expressies vereist. Reguliere expressies zijn industriestandaard, maar de specifieke implementatie verschilt per geval.

[pakket java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschrijft de specifieke regelmatige uitdrukkingsimplementatie die door Beeld Serving wordt gebruikt.

## Vastgelegde subtekenreeksen {#section-8057cd65d48949ffb6a50e929bd3688b}

Om complexe URL-wijzigingen mogelijk te maken, kunnen subtekenreeksen worden vastgelegd in de expressie door de subtekenreeks tussen haakjes (...) te plaatsen. Vastgelegde subtekenreeksen worden opeenvolgend genummerd, beginnend met 1 op basis van de positie van het voorloophaakje. De vastgelegde subtekenreeksen kunnen in de vervanging worden ingevoegd met *`$n`*, waarbij *`n`* is het volgnummer van de vastgelegde subtekenreeks.

## Bestanden met regelsets beheren {#section-e8ce976b56404c009496426fd334d23d}

Eén regelsetbestand kan aan elke materiaalcatalogus worden gekoppeld met het kenmerk Catalogus `attribute::RuleSetFile`. U kunt het regelsetbestand op elk gewenst moment bewerken, maar de afbeeldingsserver herkent de wijzigingen alleen wanneer de bijbehorende materiaalcatalogus opnieuw wordt geladen. Dit gebeurt wanneer de [!DNL Platform Server] wordt gestart of opnieuw gestart en telkens wanneer het primaire catalogusbestand (met een [!DNL .ini] achtervoegsel bestand) is gewijzigd of &#39;aangeraakt&#39; (om de bestandsdatum te wijzigen).

## Voorbeelden {#section-c4142a41f5cd4ff799a72fbc130c3700}

Voorbeelden van linialen zijn te vinden in het corresponderende gedeelte van de naslaggids voor afbeeldingscatalogi in de documentatie bij Afbeeldingsserver.

## Zie ook {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[pakket java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
