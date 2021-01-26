---
description: Rendering van afbeeldingen ondersteunt een eenvoudig voorbewerkingsmechanisme voor aanvragen dat is gebaseerd op regels voor het afstemmen van reguliere expressies en het vervangen van expressies.
seo-description: Rendering van afbeeldingen ondersteunt een eenvoudig voorbewerkingsmechanisme voor aanvragen dat is gebaseerd op regels voor het afstemmen van reguliere expressies en het vervangen van expressies.
seo-title: Referentie voor regelset
solution: Experience Manager
title: Referentie voor regelset
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# Regelsetreferentie{#rule-set-reference}

Rendering van afbeeldingen ondersteunt een eenvoudig voorbewerkingsmechanisme voor aanvragen dat is gebaseerd op regels voor het afstemmen van reguliere expressies en het vervangen van expressies.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Verzamelingen van voorverwerkingsregels (*regelsets*) kunnen worden gekoppeld aan materiaalcatalogi of de standaardcatalogus. De regels in de standaardcatalogus zijn alleen van toepassing als de aanvraag geen specifieke materiaalcatalogus bevat.

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

De elementen `<?xml>`, `<!DOCTYPE>` en `<ruleset>` worden altijd vereist in een geldig regel geplaatst dossier van XML, zelfs als geen daadwerkelijke regels worden bepaald.

Eén `<ruleset>`-element met een willekeurig aantal `<rule>`-elementen is toegestaan.

De inhoud van het voorbewerken van regelbestanden is hoofdlettergevoelig.

## URL-voorbewerking {#section-737a38d1b8c746f995e64fa6cfbcec87}

Vóór een andere verwerking, wordt een inkomende HTTP- verzoek gedeeltelijk ontleed om te bepalen welke materiaalcatalogus zou moeten worden toegepast. Nadat de catalogus is geïdentificeerd, wordt de regelset toegepast voor de geselecteerde catalogus (of de standaardcatalogus als er geen specifieke catalogus is geïdentificeerd).

De `<rule>` elementen worden gezocht in de orde die voor een gelijke met de inhoud van het `<expression>` element ( *`expression`*) wordt gespecificeerd.

Als een `<rule>` wordt aangepast, wordt de optionele *`substitution`* toegepast en wordt de gewijzigde verzoektekenreeks doorgegeven aan de verzoekparser van de server voor normale verwerking.

Als geen succesvolle gelijke wordt gemaakt wanneer het eind van `<ruleset>` wordt bereikt, wordt het verzoek overgegaan tot de parser zonder wijziging.

## Het OnMatch-kenmerk {#section-7a8ad3597780486985af5e9a3b1c7b56}

Het standaardgedrag kan worden gewijzigd met het `OnMatch`-kenmerk van de `<rule>`-elementen. `OnMatch` kan worden ingesteld op  `break` (standaard),  `continue`of  `error.`

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

## Cataloguskenmerken {#section-1f59ce84234f4576ba8473b0e6ba22ee} overschrijven

`<rule>` elementen kunnen desgewenst kenmerken definiëren die de overeenkomende cataloguskenmerken overschrijven wanneer de regel correct wordt aangepast en  `OnMatch="break"` is ingesteld. Er worden geen kenmerken toegepast wanneer `OnMatch="continue"` is ingesteld. Raadpleeg de beschrijving van `<rule>` voor een lijst met kenmerken die met regels kunnen worden beheerd.

## Reguliere expressies {#section-4d326507b52544b0960a9a5f303e3fe6}

Eenvoudige tekenreeksovereenkomsten werken voor zeer eenvoudige toepassingen, maar in de meeste gevallen zijn reguliere expressies vereist. Reguliere expressies zijn industriestandaard, maar de specifieke implementatie verschilt per geval.

[pakket java.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regexdescribes the specific Regular expression implementation used by Image Serving.

## Vastgelegde subtekenreeksen {#section-8057cd65d48949ffb6a50e929bd3688b}

Om complexe URL-wijzigingen mogelijk te maken, kunnen subtekenreeksen worden vastgelegd in de expressie door de subtekenreeks tussen haakjes (...) te plaatsen. Vastgelegde subtekenreeksen worden opeenvolgend genummerd, beginnend met 1 op basis van de positie van het voorloophaakje. De vastgelegde subtekenreeksen kunnen in de vervanging worden ingevoegd met *`$n`*, waarbij *`n`* het volgnummer van de vastgelegde subtekenreeks is.

## Bestanden {#section-e8ce976b56404c009496426fd334d23d} beheren met regelsets

Eén regelsetbestand kan aan elke materiaalcatalogus worden gekoppeld met het cataloguskenmerk `attribute::RuleSetFile`. U kunt het regelsetbestand op elk gewenst moment bewerken, maar de afbeeldingsserver herkent de wijzigingen alleen wanneer de bijbehorende materiaalcatalogus opnieuw wordt geladen. Dit gebeurt wanneer de server van het Platform wordt begonnen of opnieuw begonnen en wanneer het primaire catalogusdossier (dat een [!DNL .ini] dossierachtervoegsel heeft) wordt gewijzigd of &quot;aangeraakt&quot;(om de dossierdatum te veranderen).

## Voorbeelden {#section-c4142a41f5cd4ff799a72fbc130c3700}

Voorbeelden van linialen zijn te vinden in het corresponderende gedeelte van de naslaggids voor afbeeldingscatalogi in de documentatie bij Afbeeldingsserver.

## Zie ook {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[pakket java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
