---
title: SVG
description: De instellingen in deze sectie mogen alleen in aanmerking worden genomen als SVG-rendering vereist is.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# SVG{#svg}

De instellingen in deze sectie mogen alleen in aanmerking worden genomen als SVG-rendering vereist is.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

De Java-heapgrootte voor de SVG Renderer. De standaardwaarde is &quot;200m&quot; (200 MB).

## PS::svgProvider.rootPaths - Hoofdmapgegevens SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

De locatie van de gegevensbestanden van de SVG-bron. Dit kunnen een of meer absolute bestandspaden of paden zijn ten opzichte van *[!DNL install_folder]*, gescheiden met puntkomma&#39;s. Wordt doorgaans op dezelfde waarde ingesteld als `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Maximale bestandsgrootte SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Maximale bestandsgrootte van SVG-bron in kBytes. De server retourneert een fout wanneer wordt geprobeerd een SVG-bestand te renderen dat groter is dan deze limiet. De standaardwaarde is 1024 kBytes.

## IS::SvgMAxRenderRgnPixels - Limiet voor afbeeldingsgrootte voor SVG-uitvoer {#section-5be1fd9639424d878a5ffd11736d3920}

Hierdoor wordt de grootte beperkt van afbeeldingen die SVGRender kan produceren. Geheel getal groter dan 0 in miljoenen pixels. Er wordt een fout geretourneerd als een renderbewerking de maximale grootte zou overschrijden. De standaardwaarde is 4.

## PS::svgProvider.port - [!DNL Platform Server] Luisterpoort {#section-f7e42a96c2dd4523b46f0557c239e659}

De poort die wordt gebruikt voor SvgRender om afbeeldingen op te halen van de [!DNL Platform Server] in SVG-renderingen worden ingesloten.

Belangrijk voor het correct functioneren van de component SVGRender, moet deze configuratieoptie aan de zelfde waarde worden geplaatst `TC::PsPort`.

## PS::svgProvider.fontRoot - Map met SVG-lettertypebestanden {#section-a8d45b0d68504945b8780f5eac351b0d}

Geeft aan waar de SvgRender de lettertypebestanden vindt die nodig zijn voor het renderen van SVG-tekst; doorgaans een van de paden die zijn opgegeven in `IS::RootPaths`. Standaard is [!DNL &#x200B; *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Vormt de haven waarop de Server van het Beeld en de component SVGRender communiceren.

>[!NOTE]
>
>Voor een correcte werking van de component SVGRender moet hetzelfde poortnummer worden opgegeven voor `SVG::SVGRender.port` en `IS::SVGTcpPort`.
