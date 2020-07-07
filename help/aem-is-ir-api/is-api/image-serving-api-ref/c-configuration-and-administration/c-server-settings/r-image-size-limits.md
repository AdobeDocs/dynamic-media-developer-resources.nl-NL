---
description: Gebruik deze serverinstellingen om de limieten voor afbeeldingsgrootte in te stellen.
seo-description: Gebruik deze serverinstellingen om de limieten voor afbeeldingsgrootte in te stellen.
seo-title: Limieten voor afbeeldingsgrootte
solution: Experience Manager
title: Limieten voor afbeeldingsgrootte
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Limieten voor afbeeldingsgrootte{#image-size-limits}

Gebruik deze serverinstellingen om de limieten voor afbeeldingsgrootte in te stellen.

## IS::MaxMessageSize - Limiet voor antwoordgrootte {#section-bd942385d4d144cd904003695d72c85e}

Beperkt de grootte van gegevens de Server van het Beeld wordt toegestaan om naar de Server van het Platform te verzenden. In feite beperkt dit de grootte van de gecodeerde/gecomprimeerde reactieafbeelding die via HTTP (Mbytes) kan worden geretourneerd via Beelddeling naar de client.

## IS::MaxRenderRgnPixels - Limiet voor afbeeldingsgrootte uitvoer {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Hiermee beperkt u de grootte van afbeeldingen die de afbeeldingsserver kan maken (met uitzondering van afbeeldingen die zijn opgeslagen in het bestand). Geheel getal groter dan 0 in miljoenen pixels. Er wordt een fout geretourneerd als een renderbewerking de maximale grootte zou overschrijden. De standaardwaarde is 16.

## IS:MaxSavePixels - Limiet voor grootte voor opslaan naar bestanden {#section-d1547c4afa88467080ab08356f775e06}

Beperkt de grootte van beelden de Server van het Beeld aan dossiers met het `req=saveToFile` bevel zal schrijven. Geheel getal groter dan 0 in miljoenen pixels. Er wordt een fout geretourneerd als het bestand tijdens het opslaan deze limiet zou overschrijden. De standaardwaarde is 100 miljoen pixels.

## IS::MaxNonDsfSize - formaatlimiet voor niet-PTIFF-invoerafbeeldingen {#section-50de28a7158a436393cce5da0d1e4d46}

De maximumgrootte (in pixels) van afbeeldingen die geen PTIFF-bestanden zijn die de afbeeldingsserver mag openen. De Beeldserver retourneert een fout wanneer wordt geprobeerd toegang te krijgen tot een niet-PTIFF-afbeelding die groter is dan deze limiet.

>[!NOTE]
>
>Het plaatsen van deze waarde te hoog kan de Server van het Beeld veroorzaken om van geheugen uitgeput te zijn en in mislukkingen, met inbegrip van neerstortingen te resulteren.

