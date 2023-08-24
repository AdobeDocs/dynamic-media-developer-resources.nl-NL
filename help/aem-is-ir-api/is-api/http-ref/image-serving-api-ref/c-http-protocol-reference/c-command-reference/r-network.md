---
title: netwerk
description: Leer over het gebruiken van de optimalisering van de netwerkbandbreedte om de beeldkwaliteit aan te passen die op daadwerkelijke netwerkbandbreedte wordt gediend.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '157'
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

De bandbreedtewaarden van het netwerk zijn gebaseerd op de ontdekte cliënt-zijwaarden van gebundelde CDN.

## Eigenschappen

Een aanvraagkenmerk. Het heeft geen effect als de netvoorwaarden uitstekend zijn.

## Standaard

`network=off`

## Voorbeeld

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Zie ook

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [druppel](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Slimme afbeeldingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)