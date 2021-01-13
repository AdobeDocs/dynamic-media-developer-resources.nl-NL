---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>De serverURL malplaatje van Info wordt gebruikt om sleutel/waardeparen voor de veranderlijke vervanging in het infopaneelinhoudsmalplaatje te halen. De opgegeven sjabloon bevat doorgaans macroplaatsaanduidingen die worden vervangen door de werkelijke gegevens voordat het verzoek naar de server wordt verzonden. </p> <p><span class="codeph"> $1$</span> is vervangen door de het omvergooienwaarde die  <span class="codeph"> </span> InfoPanelPopupactivation teweegbracht. </p> <p><span class="codeph"> $2$</span> wordt vervangen door het volgnummer van het huidige frame in de afbeeldingsset. </p> <p><span class="codeph"> $3$</span> is vervangen door het eerste wegelement dat in de naam van de ouderreeks van het huidige punt wordt gespecificeerd. Deze komt meestal overeen met de catalogus-id. </p> <p><span class="codeph"> $4$</span> is vervangen door het volgende element in de weg en beantwoordt aan activa identiteitskaart De eigenlijke aanvraagsyntaxis van de infoserver is afhankelijk van de infoserver en verschilt van server tot server. Hier volgt bijvoorbeeld een standaardaanvraagsjabloon voor een Scene7 info-server: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Houd er rekening mee dat wanneer u de pop-up van het deelvenster Info configureert, de HTML-code en de JavaScript-code die aan het deelvenster Info zijn doorgegeven, op de computer van de client worden uitgevoerd. Zorg daarom dat dergelijke HTML-code en JavaScript-code veilig zijn.

## Eigenschappen {#section-71356e3c13244e62b0582980d9d05328}

Optioneel.

## Standaard {#section-22e9af803f724434807d34e200eb7518}

Geen.

## Voorbeeld {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
