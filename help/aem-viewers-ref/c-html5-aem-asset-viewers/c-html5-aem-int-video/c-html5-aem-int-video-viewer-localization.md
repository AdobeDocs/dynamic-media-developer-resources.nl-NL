---
description: Bepaalde inhoud die in de Interactive Video Viewer wordt weergegeven, is afhankelijk van lokalisatie. Hier volgen knopinfo voor gebruikersinterface-elementen en een foutbericht dat wordt weergegeven wanneer de video niet kan worden afgespeeld.
seo-description: Bepaalde inhoud die in de Interactive Video Viewer wordt weergegeven, is afhankelijk van lokalisatie. Hier volgen knopinfo voor gebruikersinterface-elementen en een foutbericht dat wordt weergegeven wanneer de video niet kan worden afgespeeld.
seo-title: Lokalisatie van gebruikersinterface-elementen
solution: Experience Manager
title: Lokalisatie van gebruikersinterface-elementen
topic: Dynamic media
uuid: 7c880e25-76dc-43d3-83fc-12de92afd35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de Interactive Video Viewer wordt weergegeven, is afhankelijk van lokalisatie. Hier volgen knopinfo voor gebruikersinterface-elementen en een foutbericht dat wordt weergegeven wanneer de video niet kan worden afgespeeld.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door de speciale Viewer SDK-id SYMBOL. Elk SYMBOL heeft een aan de standaard gekoppelde tekstwaarde voor een Engelse landinstelling ( `"en"`) die wordt geleverd met de viewer buiten de box en kan ook door de gebruiker gedefinieerde waarden hebben ingesteld voor zoveel landinstellingen als nodig.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te controleren of er voor elke ondersteunde SYMBOL-landinstelling een door de gebruiker gedefinieerde waarde is. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Dit object bevat een lijst met ondersteunde landinstellingen, SYMBOL-tekstwaarden voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject is het volgende:

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt het lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De code van de webpagina moet het lokalisatieobject doorgeven aan de viewerconstructor als een waarde van het veld `localizedTexts` van het configuratieobject. Een andere optie is om het lokalisatieobject door te geven door de methode `setLocalizedTexts(localizationInfo)` aan te roepen.

De volgende SYMBOL&#39;s worden ondersteund:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOOL </p> </th> 
   <th colname="col2" class="entry"> <p>Knopinfo voor... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-label voor viewerelement op hoofdniveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Geselecteerde knopstatus voor afspelen pauzeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Niet geselecteerd knopstatus Afspelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p> De status van de pauzeknop opnieuw afspelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Video scrubber. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Videotijd op besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Geselecteerd veranderbaar volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Niet-geselecteerd veranderbaar volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p> Label van de volumeschuifregelaar dat wordt weergegeven met het kenmerk <span class="codeph"> aria-valueText </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>De knop Volledig scherm in normale toestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>De knop Volledig scherm in volledige schermstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Geselecteerde knopstatus voor gesloten bijschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Niet-geselecteerde knopstatus voor gesloten bijschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER  </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>De knop Omhoog schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Omlaag schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Gereedschap Sociaal delen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Delen van koppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Koptekst van dialoogvenster Koppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Knop rechtsboven in het dialoogvenster Koppeling sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschrijving van de aandeelkoppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>De knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Alles selecteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Selecteer Alles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Delen via Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Twitter delen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten van deelvenster Handelingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>Foutbericht dat wordt weergegeven wanneer video niet kan worden afgespeeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

