---
description: Hiermee werkt u de instellingen voor de vignetpublicatie-indeling bij.
seo-description: Hiermee werkt u de instellingen voor de vignetpublicatie-indeling bij.
seo-title: updateVignetPublishFormat
solution: Experience Manager
title: updateVignetPublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateVignetPublishFormat{#updatevignettepublishformat}

Hiermee werkt u de instellingen voor de vignetpublicatie-indeling bij.

## Geautoriseerde gebruikerstypen {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignetPublishFormatParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Ja | Handgreep voor publicatie-indeling. |
| ` *`name`*` | `xsd:string` | Nee | Naam van publicatie-indeling. |
| ` *`targetWidth`*` | `xsd:int` | Ja | Geeft de doelbreedte van de resulterende vignetweergave op in pixels. Gebruik nul, zodat het uitvoervignet dezelfde grootte heeft als het hoofdvignet. |
| ` *`targetHeight`*` | `xsd:int` | Ja | Hiermee stelt u de doelhoogte van de resulterende vignetweergave in pixels in. Gebruik nul, zodat het uitvoervignet dezelfde grootte heeft als het hoofdvignet. |
| ` *`createPyramid`*` | `xsd:boolean` | Ja | Hiermee maakt u een piramidevignet dat is geoptimaliseerd voor zoomen op de server voor het renderen van afbeeldingen. Vanaf de maximale grootte, ingesteld door de velden Doelgrootte vignet, maakt dit meerdere grootteweergaven in één vignetuitvoerbestand. Elke volgende weergavegrootte wordt gehalveerd totdat de breedte en hoogte binnen 128 x 128 pixels liggen. |
| ` *`thumbWidth`*` | `xsd:int` | Ja | Geeft de breedte van elke resulterende miniatuur in pixels aan. Deze instelling is optioneel. Geen miniatuurbestand gebruiken als nul. |
| ` *`saveAsVersion`*` | `xsd:int` | Ja | Hier geeft u de bestandsindeling voor de gepubliceerde vignetten op. Op basis van een nieuwe versie van Image Authoring en een oudere versie van Image Rendering Server moet u een vignetversie opgeven die uw ImageRendering Server kan lezen. Als u een hogere versie opgeeft, kan de server voor het renderen van afbeeldingen de gepubliceerde vignetten niet lezen. Stel dit in op nul om vignetten te publiceren in de meest recente versie. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | Ja | Hiermee geeft u het teken op dat de naam van het vignet scheidt van het achtervoegsel dat de breedte aangeeft. |
| ` *`verscherpen`*` | `xsd:int` | Nee | Hiermee past u verscherping toe op de hoofdafbeelding van de weergave voor elke grootte van het publicatievenster. Verscherpen kan vervaging compenseren wanneer de vignetten worden geschaald. |
| ` *`usmAmount`*` | `xsd:double` | Ja | Digitaal onscherp maskeren is een flexibele en krachtige manier om de scherpte te verhogen, vooral in gescande afbeeldingen. Hiermee bepaalt u de grootte van elke overschrijding (hoe veel donkerder en lichter de randen worden). |
| ` *`usmRadius`*` | `xsd:double` | Ja | Heeft invloed op de grootte van de randen die worden vergroot of op de breedte van de randranden. Hierdoor wordt de gedetailleerdheid van de randen vergroot door een kleinere straal. Hogere straalwaarden kunnen halo&#39;s aan de randen veroorzaken. Voor fijne details is een kleinere straal nodig, omdat kleine details van dezelfde grootte of kleiner dan de straal verloren gaan. |
| ` *`usmThreshold`*` | `xsd:int` | Ja | Hiermee bepaalt u de minimale helderheidswijziging die moet worden verscherpt of de afstand tussen aangrenzende toonwaarden voordat het filter werkt. Met deze instelling kunt u scherpere randen verscherpen terwijl u subtielere randen ongewijzigd laat. Het toegestane bereik van de drempel is 0 tot en met 255. |

**Output (updateVignetPublishFormatReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Ja | Verwerk de bijgewerkte publicatie-indeling van het vignet. |

## Voorbeeld {#section-fcba4bf2b7264786a676e315a35dbe43}

In dit codevoorbeeld wordt een vignetpublicatie-indeling bijgewerkt en wordt de greep teruggezet naar de bijgewerkte indeling.

**Verzoek**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Antwoord**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```

