---
title: dpr
description: DPR (Device Pixel Ratio)&mdash;ook wel CSS-pixelverhouding&mdash genoemd;is de relatie tussen de fysieke pixels van een apparaat en logische pixels.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# dpr{#dpr}

De pixelverhouding van het apparaat (DPR), ook wel CSS-pixelverhouding genoemd, is de verhouding tussen de fysieke pixels van een apparaat en logische pixels. Vooral met de komst van Retina-schermen groeit de pixelresolutie van moderne mobiele apparaten snel.

Als u de pixelverhouding van het apparaat inschakelt, wordt de afbeelding weergegeven met de oorspronkelijke resolutie van het scherm, waardoor deze scherp wordt.

Momenteel is de pixeldichtheid van het beeldscherm afkomstig van Akamai CDN-headerwaarden.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> uit </span> </span> </p> </td> 
  <td class="stentry"> <p>Schakel DPR-optimalisatie op individueel afbeeldings-URL-niveau uit. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Overschrijf de DPR-waarde die door Smart Imaging wordt gedetecteerd, met een aangepaste waarde (zoals wordt gedetecteerd door elke logica aan de clientzijde of andere methode). Toegestane waarde voor dprValue is een getal groter dan 0. </p> </td> 
 </tr> 
</table>


U kunt `dpr=on,dprValue` zelfs als het bedrijf de DPR-instelling als uitgeschakeld heeft.

Als de resulterende afbeelding door DPR-optimalisatie groter is dan de Dynamic Media-instelling MaxPix, wordt de breedte van MaxPix altijd herkend door de hoogte-breedteverhouding van de afbeelding te behouden.

| Aangevraagde afbeeldingsgrootte | DPR-waarde | Afgeleverde afbeeldingsgrootte |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR-waarden zijn gebaseerd op de gedetecteerde client-side waarden van de gebundelde CDN. Deze waarden zijn soms onjuist. IPhone5 bijvoorbeeld met `dpr=2`en iPhone12 met dpr=3, beide tonen `dpr=2`. Stilstaand, voor apparaten met hoge resolutie, verzenden `dpr=2` is beter dan verzenden `dpr=1`. De beste manier om deze onnauwkeurigheid te overwinnen, is echter door DPR op de client-side te gebruiken om u 100% nauwkeurige waarden te geven. En het werkt voor elk apparaat, of het nu Apple is of een ander apparaat dat gelanceerd werd. Zie [Slimme beeldverwerking gebruiken met pixelverhouding van client-side apparaat](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=nl-NL).

## Eigenschappen

Een aanvraagkenmerk. Het heeft geen effect als `dpr` is uit of als `dprValue=1`.

## Standaard

`dpr=off`


## Voorbeeld

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Zie ook

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [netwerk](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Slimme afbeeldingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=nl-NL)