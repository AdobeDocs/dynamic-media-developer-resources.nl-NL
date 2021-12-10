---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>De serverURL malplaatje van Info wordt gebruikt om sleutel/waardeparen voor de veranderlijke vervanging in het infopaneelinhoudsmalplaatje te halen. De opgegeven sjabloon bevat doorgaans macroplaatsaanduidingen die worden vervangen door de werkelijke gegevens voordat het verzoek naar de server wordt verzonden. </p> <p><span class="codeph"> $1$</span> wordt vervangen door de rollover-waarde die de <span class="codeph"> InfoPanelPopup</span> activering. </p> <p><span class="codeph"> $2$</span> wordt vervangen door het volgnummer van het huidige frame in de afbeeldingsset. </p> <p><span class="codeph"> $3$</span> wordt vervangen door het eerste padelement dat is opgegeven in de naam van de bovenliggende set van het huidige item. Deze komt meestal overeen met de catalogus-id. </p> <p><span class="codeph"> $4$</span> wordt vervangen door het volgende element in het pad en komt overeen met de element-id. De eigenlijke aanvraagsyntaxis van de infoserver is afhankelijk van de infoserver en verschilt van server tot server. Hier volgt bijvoorbeeld een standaardaanvraagsjabloon voor een Dynamic Media info-server: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wanneer u het Pop-up van het deelvenster Info configureert, worden de HTML-code en JavaScript-code die aan het deelvenster Info zijn doorgegeven, uitgevoerd op de computer van de client. Controleer daarom of dergelijke HTML-code en JavaScript-code veilig zijn.

## Eigenschappen {#section-71356e3c13244e62b0582980d9d05328}

Optioneel.

## Standaard {#section-22e9af803f724434807d34e200eb7518}

Geen.

## Voorbeeld {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
