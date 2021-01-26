---
description: Pas de afbeeldingsdekking aan. Hiermee kunt u de voorgronddekking van een afbeeldings-, tekst-, effen kleur- of effectlaag verlagen.
seo-description: Pas de afbeeldingsdekking aan. Hiermee kunt u de voorgronddekking van een afbeeldings-, tekst-, effen kleur- of effectlaag verlagen.
seo-title: opac
solution: Experience Manager
title: opac
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# opac{#opac}

Pas de afbeeldingsdekking aan. Hiermee kunt u de voorgronddekking van een afbeeldings-, tekst-, effen kleur- of effectlaag verlagen.

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> dekking</span> </p> </td> 
  <td class="stentry"> <p>Primaire dekking (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Dekking vulling (0...100 int). </p></td> 
 </tr> 
</table>

De voorgronddekking voor een afbeeldingslaag wordt bepaald door het laagmasker of het alfakanaal van de afbeelding, of als geen van beide aanwezig zijn, is de dekking 100%. De voorgronddekking van een tekstlaag is 100% en die van een effen kleurlaag wordt ingesteld op `color=`.

`opac=` Hiermee wijzigt u nooit de dekking van gebieden die zijn gevuld met  `color=` of  `bgColor=`, behalve de voorgrondgebieden van effen kleuren en effectlagen (ingesteld met  `color=`).

Als *`opacity`* wordt opgegeven in een afbeelding, tekst of effen kleurlaag, wordt de gehele laag toegepast, inclusief alle bijbehorende effectlagen, terwijl *`fillOpacity`* alleen van toepassing is op de inhoud van de primaire laag. Wanneer opgegeven in een effectlaag, wordt *`opacity`* toegepast op de effectlaag, terwijl *`fillOpacity`* wordt genegeerd.

De effectieve dekking voor de inhoud van de hoofdlaag is ( *`opacity`* * *`fillOpacity`* / 100). De effectieve dekking voor effectlagen is (main *`opacity`* * effect *`opacity`* / 100).

## Eigenschappen {#section-ac3f136ff1584a2eab87500b7164f7fa}

Laagkenmerk. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`.

## Standaard {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, voor geen wijziging in de laagdekking.

## Voorbeeld {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

De tekstdekking in dit voorbeeld is 90*70/100=63% en de dekking van de effectlaag is 90*50/100=45%.

## Zie ook {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
