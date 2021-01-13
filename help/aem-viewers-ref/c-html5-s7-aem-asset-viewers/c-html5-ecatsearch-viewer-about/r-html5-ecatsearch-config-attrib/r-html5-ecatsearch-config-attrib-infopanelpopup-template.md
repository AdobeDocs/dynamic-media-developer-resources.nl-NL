---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
topic: Dynamic media
uuid: a7b49f82-9a8b-45f8-b933-9880659770de
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`template`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> template</span></span> </p> </td> 
   <td> <p>De inhoudssjabloon waarin de gegevens die door de infoserver worden geretourneerd, worden samengevoegd. </p> <p>De inhoudssjabloon is een XML die volgt op deze DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>De werkelijke syntaxis voor de inhoudssjabloon is als volgt: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Dat wil zeggen dat de sjabloon moet beginnen met het <span class="codeph"> &lt;info&gt;</span>-element dat optionele standaard <span class="codeph"> &lt;var&gt;</span>-elementen kan bevatten. De sjablooninhoud zelf, <span class="codeph"> TEMPLATE_CONTENT</span> is HTML-tekst. Daarnaast kan de inhoudssjabloon namen van variabelen bevatten die zijn opgenomen in <span class="codeph"> $</span> tekens. Deze tekens worden vervangen door de waarden van de variabelen die door de infoserver worden geretourneerd of door de standaardwaarden. </p> <p>Standaardvariabelen die in de sjabloon zijn gedefinieerd, kunnen globaal zijn (als het rollover-kenmerk niet is ingesteld) of specifiek zijn voor een bepaalde rollover-sleutel (als het rollover-kenmerk aanwezig is). </p> <p>Tijdens sjabloonverwerkingsvariabelen die specifiek zijn voor rollover-sleutels hebben voorrang op algemene variabelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Houd er rekening mee dat wanneer u de pop-up van het deelvenster Info configureert, de HTML-code en de JavaScript-code die aan het deelvenster Info zijn doorgegeven, op de computer van de client worden uitgevoerd. Zorg daarom dat dergelijke HTML-code en JavaScript-code veilig zijn.

## Eigenschappen {#section-6dd7785357d740d095fa9f7fd0f67da4}

Optioneel.

## Standaard {#section-cd5db06d08aa4de49e37d6c938b41570}

Geen.

## Voorbeeld {#section-16d184665c484964af9a22f79ff3f840}

Ervan uitgaande dat de infoserver-reactie de productnaam als variabele `$1$` retourneert en de URL van de productafbeelding als variabele `$2$` wordt geretourneerd.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
