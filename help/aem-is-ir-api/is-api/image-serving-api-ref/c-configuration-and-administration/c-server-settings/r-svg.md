---
description: De instellingen in deze sectie hoeven alleen in overweging te worden genomen als SVG-rendering is vereist.
seo-description: De instellingen in deze sectie hoeven alleen in overweging te worden genomen als SVG-rendering is vereist.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# SVG{#svg}

De instellingen in deze sectie hoeven alleen in overweging te worden genomen als SVG-rendering is vereist.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

De Java-heapgrootte voor de SVG Renderer. De standaardwaarde is &quot;200m&quot; (200 Mbytes).

## PS::svgProvider.rootPaths - SVG-hoofdmappen voor gegevens {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

De locatie van de SVG-brongegevensbestanden. Kan een of meer absolute bestandspaden of paden zijn ten opzichte van *[!DNL install_folder]*, gescheiden met puntkomma&#39;s. Wordt doorgaans ingesteld op dezelfde waarde als `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Maximale SVG-bestandsgrootte {#section-b9c81e3e104642ebbdd9f000843d3256}

Maximale SVG-bronbestandsgrootte in kBytes. De server retourneert een fout wanneer wordt geprobeerd een SVG-bestand te renderen dat groter is dan deze limiet. De standaardwaarde is 1024 kBytes.

## IS::SvgMAxRenderRgnPixels - Limiet SVG-uitvoerafbeelding {#section-5be1fd9639424d878a5ffd11736d3920}

Hiermee beperkt u de grootte van afbeeldingen die SVGRender kan produceren. Geheel getal groter dan 0 in miljoenen pixels. Er wordt een fout geretourneerd als een renderbewerking de maximale grootte zou overschrijden. De standaardwaarde is 4.

## PS::svgProvider.port - Poort voor luisteren naar server van Platform {#section-f7e42a96c2dd4523b46f0557c239e659}

De poort die wordt gebruikt voor SvgRender om afbeeldingen op te halen van de server van het Platform die moet worden ingesloten in SVG-renderingen.

Belangrijk voor het correct functioneren van de component SVGRender, moet deze configuratieoptie aan de zelfde waarde zoals `TC::PsPort` worden geplaatst.

## PS::svgProvider.fontRoot - Map SVG Font Files {#section-a8d45b0d68504945b8780f5eac351b0d}

Hiermee geeft u aan waar de SvgRender de lettertypebestanden moet zoeken die nodig zijn voor het weergeven van SVG-tekst. doorgaans een van de paden die worden opgegeven in `IS::RootPaths`. De standaardwaarde is [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Vormt de haven waarop de Server van het Beeld en de component SVGRender communiceren.

>[!NOTE]
>
>Voor een correcte werking van de component SVGRender moet hetzelfde poortnummer worden opgegeven voor `SVG::SVGRender.port` en `IS::SVGTcpPort`.

