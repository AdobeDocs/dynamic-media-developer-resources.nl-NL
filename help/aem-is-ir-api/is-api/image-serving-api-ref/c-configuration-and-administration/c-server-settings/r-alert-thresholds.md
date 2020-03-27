---
description: Gebruik deze servermontages om waakzame drempels te vormen.
seo-description: Gebruik deze servermontages om waakzame drempels te vormen.
seo-title: Waarschuwingsdrempels
solution: Experience Manager
title: Waarschuwingsdrempels
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Waarschuwingsdrempels{#alert-thresholds}

Gebruik deze servermontages om waakzame drempels te vormen.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Er wordt een waarschuwing over de responstijd weergegeven wanneer de gemiddelde tijd die nodig is om een aanvraag tijdens het monsterinterval te verwerken, de hier vastgestelde drempelwaarde overschrijdt. uitgedrukt in msec; geheel getal 0 of groter. De typische waarden liggen tussen 100 en 1000 msec, afhankelijk van de ingewikkeldheid van verrichtingen.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Voor deze waarschuwing worden geen verzoeken in overweging genomen die resulteren in 4xx- of 5xx-reactiestatus.

## AS::monitorAlertGenerator.maxErrorRate - Foutresponspercentage DrempelAS::monitorAlertGenerator.maxErrorRate - Foutresponspercentage {#section-76ba77fd3102419395e0f86719a1f3ec}

Er wordt een foutmelding weergegeven wanneer de verhouding tussen de HTTP-foutreacties en de totale responsen tijdens het samplinginterval de opgegeven drempel overschrijdt.

Reële waarde tussen 0,0 en 1,0. Wordt meestal ingesteld op tussen 0,005 en 0,1. Stel in op 1 om foutwaarschuwingen uit te schakelen.

## AS::monitorAlertGenerator.minRequestRate - Lage verkeersdrempel {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Er wordt een minimale verkeerswaarschuwing verzonden wanneer het gemiddelde aantal ontvangen verzoeken per seconde tijdens het huidige steekproefinterval onder deze drempel daalt. Schakel de waarschuwing uit door deze waarde in te stellen op 0. Uitgedrukt in aanvragen per seconde. Reële waarde 0 of hoger.

## AS:monitorAlertGenerator.minFreeHeapSpace -Free Heap Space Threshold {#section-ce6705045f6842769030ccb1894594cc}

Hiermee geeft u de minimale vrije Java-heapruimte op. Er wordt direct na een Java-opschooncyclus een prioriteitswaarschuwing verzonden wanneer de vrije heapruimte onder deze drempelwaarde ligt. 50 MB wordt geadviseerd voor veilige verrichting van de Server van het Platform. Als u de vrije heapruimte boven deze waarde houdt, neemt de frequentie van de afvalophalingscycli af, wat de algehele serverprestaties kan verbeteren. Geheel getal in bytes, 0 of groter.

## AS::monitorAlertGenerator.maxOverlap - Maximum aantal gelijktijdige verzoeken {#section-ddc6925bff944758ab19bcc9cf3f2589}

Een overlappende waarschuwing wordt teweeggebracht wanneer het gemiddelde aantal verzoeken gelijktijdig tijdens het middelingsinterval wordt verwerkt deze drempel overschrijdt. Een hoge overlapping kan wijzen op een mogelijke voorwaarde van de serveroverbelasting.

Geheel getal 1 of groter. Het bereik is doorgaans 20 tot 50, afhankelijk van de aanraaksnelheid in cache en de compexiteit van de aanvraag.

## AS:monitorAlertGenerator.lockedThreshold - Vergrendelde aanvraagdrempel {#section-012a1c9937d445708380339279c62d80}

Geeft het aantal seconden aan dat een aanvraag in behandeling moet zijn voordat deze wordt beschouwd als vergrendeld of gekoppeld. Een vergrendelde-aanvraagwaarschuwing wordt gegeven als aan het einde van een gemiddeld interval ten minste één verzoek langer dan de opgegeven periode in behandeling is geweest. Positieve gehele waarde in msec.

Om rekening te houden met complexe renderverzoeken en verzoeken die het verkrijgen van gegevens van buitenlandse servers van HTTP impliceren, wordt het geadviseerd om deze waarde aan minstens 30 seconden te plaatsen (tenzij een dergelijke voorwaarde door deze alarm moet worden ontdekt).
