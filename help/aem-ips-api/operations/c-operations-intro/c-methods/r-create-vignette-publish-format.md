---
description: Hiermee maakt u een nieuwe publicatie-indeling voor een vignet.
seo-description: Hiermee maakt u een nieuwe publicatie-indeling voor een vignet.
seo-title: createVignetPublishFormat
solution: Experience Manager
title: createVignetPublishFormat
topic: Dynamic Media Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# createVignetPublishFormat{#createvignettepublishformat}

Hiermee maakt u een nieuwe publicatie-indeling voor een vignet.

Vignetformaten specificeren de grootte van gepubliceerde vignettes en hun duimnagels, evenals gezoemniveaus, verscherpende parameters, en de dossierformaatversie voor vignetten die van primaire vignetten worden geproduceerd die aan een Beeld teruggevend server van IPS worden gepubliceerd.

Nieuwere versies van de server voor het renderen van afbeeldingen kunnen piramidevignetten ondersteunen, waardoor het niet nodig is specifieke grootten voor vignetten voor publicatie te definiëren.

## Toegestane gebruikerstypen {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Input (createVignetPublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Vereist </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handgreep aan het bedrijf het vignet tot behoort. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Naam om de indeling voor het publiceren van het vignet te identificeren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Geeft de doelbreedte van de resulterende vignetweergave op in pixels. </p> <p>Gebruik nul, zodat het uitvoervignet dezelfde grootte heeft als het primaire vignet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hiermee maakt u een piramidevignet dat is geoptimaliseerd voor zoomen op de server voor het renderen van afbeeldingen. Vanaf de maximale grootte, ingesteld door de velden Doelgrootte vignet, maakt dit meerdere grootteweergaven in één vignetuitvoerbestand. Elke volgende weergavegrootte wordt gehalveerd totdat de breedte en hoogte binnen 128 x 128 pixels liggen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Geeft de breedte van elke resulterende miniatuur in pixels aan. Deze instelling is optioneel. Geen miniatuurbestand gebruiken als nul. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hier geeft u de bestandsindeling voor de gepubliceerde vignetten op. Op basis van een nieuwe versie van Image Authoring en een oudere versie van de Image Rendering Server moet u een vignetversie opgeven die uw ImageRendering Server kan lezen. Als u een hogere versie opgeeft, kan de server voor het renderen van afbeeldingen de gepubliceerde vignetten niet lezen. Stel dit in op nul om vignetten te publiceren in de meest recente versie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hiermee geeft u het teken op dat wordt gescheiden door de naam van het vignet en het achtervoegsel dat de breedte aangeeft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hiermee geeft u het teken op dat wordt gescheiden door de naam van het vignet en het achtervoegsel dat de breedte aangeeft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> verscherpen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Hiermee past u verscherping toe op de hoofdafbeelding van de weergave voor elke verscherping van het vignet, waardoor vervaging kan worden gecompenseerd wanneer de vignetters worden geschaald. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Digitaal onscherp maskeren is een flexibele en krachtige manier om de scherpte te verhogen, vooral in gescande afbeeldingen. Hiermee bepaalt u de grootte van elke overschrijding (hoeveel donkerder en licht de randen worden). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Heeft invloed op de grootte van de randen die moeten worden vergroot of op de breedte van de randranden, zodat een kleiner radium de details op kleinere schaal verbetert. Hogere straalwaarden kunnen halo's aan de randen veroorzaken. Voor fijne details is een kleinere straal nodig, omdat kleine details van dezelfde grootte of kleiner dan de straal verloren gaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codewoordgroep  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hiermee bepaalt u de minimale helderheidswijziging die moet worden verscherpt of de afstand tussen aangrenzende toonwaarden voordat het filter werkt. Met deze instelling kunt u scherpere randen verscherpen terwijl u subtielere randen ongewijzigd laat. Het toegestane bereik van de drempelwaarde 0 tot en met 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignetPublishFormatReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | De handgreep naar de gemaakte vignetindeling. |

## Voorbeelden {#section-0564752d439642b9bb8de2903db6de1e}

Met deze code maakt u een vignetpublicatie-indeling. In de aanmaakaanvraag worden een naam, doelbreedte en -hoogte en andere vereiste waarden opgegeven.

**Verzoek**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Antwoord**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

