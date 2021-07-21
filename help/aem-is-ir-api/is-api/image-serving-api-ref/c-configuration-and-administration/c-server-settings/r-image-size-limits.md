---
description: Gebruik deze serverinstellingen om de limieten voor afbeeldingsgrootte in te stellen.
solution: Experience Manager
title: Limieten voor afbeeldingsgrootte
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Limieten voor afbeeldingsgrootte{#image-size-limits}

Gebruik deze serverinstellingen om de limieten voor afbeeldingsgrootte in te stellen.

## IS::MaxMessageSize - Limiet voor antwoordgrootte {#section-bd942385d4d144cd904003695d72c85e}

Beperkt de grootte van gegevens de Server van het Beeld wordt toegestaan om naar de Server van het Platform te verzenden. In feite beperkt dit de grootte van de gecodeerde/gecomprimeerde reactieafbeelding die via HTTP (Mbytes) kan worden geretourneerd via Beelddeling naar de client.

## IS::MaxRenderRgnPixels - Limiet voor afbeeldingsgrootte uitvoer {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Hiermee beperkt u de grootte van afbeeldingen die de afbeeldingsserver kan maken (met uitzondering van afbeeldingen die zijn opgeslagen in het bestand). Geheel getal groter dan 0 in miljoenen pixels. Er wordt een fout geretourneerd als een renderbewerking de maximale grootte zou overschrijden. De standaardwaarde is 16.

## IS:MaxSavePixels - Limiet voor grootte voor opslaan naar bestanden {#section-d1547c4afa88467080ab08356f775e06}

Beperkt de grootte van beelden de Server van het Beeld aan dossiers met `req=saveToFile` bevel zal schrijven. Geheel getal groter dan 0 in miljoenen pixels. Er wordt een fout geretourneerd als het bestand tijdens het opslaan deze limiet zou overschrijden. De standaardwaarde is 100 miljoen pixels.

## IS::MaxNonDsfSize - formaatlimiet voor niet-PTIFF-invoerafbeeldingen {#section-50de28a7158a436393cce5da0d1e4d46}

De maximumgrootte (in pixels) van afbeeldingen die geen PTIFF-bestanden zijn die de afbeeldingsserver mag openen. De Beeldserver retourneert een fout wanneer wordt geprobeerd toegang te krijgen tot een niet-PTIFF-afbeelding die groter is dan deze limiet.

>[!NOTE]
>
>Het plaatsen van deze waarde te hoog kan de Server van het Beeld veroorzaken om van geheugen uitgeput te zijn en in mislukkingen, met inbegrip van neerstortingen te resulteren.
