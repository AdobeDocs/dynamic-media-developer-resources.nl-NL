---
title: netwerk
description: Leer over het gebruiken van de optimalisering van de netwerkbandbreedte om de beeldkwaliteit aan te passen die op daadwerkelijke netwerkbandbreedte wordt gediend.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# netwerk{#network}

Als u Netwerkbandbreedte inschakelt, wordt automatisch de beeldkwaliteit aangepast die wordt aangeboden op basis van de werkelijke netwerkbandbreedte. Voor slechte netwerkbandbreedte, [DPR (Pixelverhouding apparaat)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) optimalisatie wordt automatisch uitgeschakeld, zelfs als deze al is ingeschakeld.

Uw bedrijf kan desgewenst de optimalisatie van de netwerkbandbreedte op het individuele beeldniveau uitschakelen door het toevoegen `network=off` naar de URL van de afbeelding.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Geeft aan of netwerkbandbreedte de beeldkwaliteit aanpast die wordt aangeboden op basis van de werkelijke netwerkbandbreedte (ingeschakeld), of dat optimalisatie van de netwerkbandbreedte is uitgeschakeld zonder aanpassing van de beeldkwaliteit.</p> </td> 
 </tr> 
</table>

DPR en de waarden van de netwerkbandbreedte zijn gebaseerd op de ontdekte cliënt-zijwaarden van gebundelde CDN. Deze waarden zijn soms onjuist. IPhone5 bijvoorbeeld met `dpr=2`en iPhone12 met `dpr=3`, beide presentaties `dpr=2`. Stilstaand, voor apparaten met hoge resolutie, verzenden `dpr=2` is beter dan dpr=1 verzenden. De beste manier om deze onnauwkeurigheid te overwinnen, is echter door DPR op de client-side te gebruiken om u 100% nauwkeurige waarden te geven. En het werkt voor elk apparaat, of het nu Apple is of een ander apparaat dat gelanceerd werd. Zie [Slimme beeldverwerking gebruiken met pixelverhouding van client-side apparaat](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Eigenschappen



## Standaard

`network=off`

## Voorbeeld

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Zie ook

[druppel](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Slimme afbeeldingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)