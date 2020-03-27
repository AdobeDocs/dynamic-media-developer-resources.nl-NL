---
description: Bepaalde inhoud die in de eCatalog Viewer wordt weergegeven, is afhankelijk van een lokalisatie, zoals zoomknoppen, knoppen voor het wijzigen van de pagina, miniatuurknop, knop Volledig scherm, knop Sluiten en schuifbalkknoppen.
seo-description: Bepaalde inhoud die in de eCatalog Viewer wordt weergegeven, is afhankelijk van een lokalisatie, zoals zoomknoppen, knoppen voor het wijzigen van de pagina, miniatuurknop, knop Volledig scherm, knop Sluiten en schuifbalkknoppen.
seo-title: Lokalisatie van gebruikersinterface-elementen
solution: Experience Manager
title: Lokalisatie van gebruikersinterface-elementen
topic: Dynamic media
uuid: bd95c7dc-3158-4cca-81d4-f5efd57c0124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de eCatalog Viewer wordt weergegeven, is afhankelijk van een lokalisatie, zoals zoomknoppen, knoppen voor het wijzigen van de pagina, miniatuurknop, knop Volledig scherm, knop Sluiten en schuifbalkknoppen.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door een speciale viewer-SDK-id met de naam SYMBOL. Aan elk SYMBOL is een standaardtekstwaarde gekoppeld voor de landinstelling Engels ( `"en"`) die wordt geleverd met de viewer buiten het vak. Bovendien kunnen er door de gebruiker gedefinieerde waarden worden ingesteld voor zoveel landinstellingen als nodig is.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te zien of er een door de gebruiker gedefinieerde waarde is voor elk ondersteund SYMBOL in de landinstelling. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Een dergelijk object bevat een lijst met ondersteunde landinstellingen, SYMBOL-tekstwaarden voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt het lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De code van de webpagina moet een dergelijk lokalisatieobject doorgeven aan de viewerconstructor als een waarde van het `localizedTexts` veld van het configuratieobject. Een andere optie is om het lokalisatieobject door te geven door `setLocalizedTexts(localizationInfo)` methode aan te roepen.

De volgende SYMBOL&#39;s worden ondersteund (ervan uitgaande dat containerId de id van de viewercontainer is):

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOOL </p> </th> 
   <th colname="col2" class="entry"> <p>Knopinfo voor... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-label voor het viewerelement op het hoogste niveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rolbeschrijving voor de hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Inzoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Uitzoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Zoomen opnieuw instellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>De knop Volledig scherm in normale toestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>De knop Volledig scherm in volledige schermstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>De knop Omhoog schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Omlaag schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_rightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Grote knop Volgende pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_leftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Grote knop Vorige pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_lastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Laatste pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondLastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Laatste pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_firstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Eerste pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondFirstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Eerste pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarRightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Volgende pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Vorige pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Knop Miniaturen in de miniatuurmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>De knop Miniaturen in de normale modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten deelvenster Info. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Gereedschap Sociaal delen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop E-maildelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Koptekst van dialoogvenster E-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Knop E-maildialoogvenster rechtsboven sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS </span> </p> </td> 
   <td colname="col2"> <p>Foutbericht weergegeven als het e-mailadres onjuist is geformuleerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>Label voor het invoerveld "Aan". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Voeg nog een e-mailadres toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>Voeg nog een e-mailadres toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>Van invoerveld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>Veld voor berichtinvoer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Knop E-mailadres verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>De knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Alles selecteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Selecteer Alles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de sluitknop die onder in het dialoogvenster wordt weergegeven nadat het formulier is verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>De knop Sluiten die onder aan het dialoogvenster wordt weergegeven nadat het formulier is verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop voor het verzenden van formulieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Knop Formulier verzenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>Bevestigingsbericht weergegeven wanneer e-mail is verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>Foutbericht dat wordt weergegeven wanneer e-mail niet is verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Delen insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Koptekst van dialoogvenster Insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten rechtsboven in het dialoogvenster Insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Beschrijving van de tekst van de ingesloten code. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Label voor de keuzelijst Grootte insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>De knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Tekst voor het laatste item "aangepaste grootte" in het invoervak Grootte insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Delen van koppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Koptekst van dialoogvenster Koppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Knop rechtsboven in het dialoogvenster Koppeling sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Beschrijving van de aandeelkoppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>De knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Alles selecteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Selecteer Alles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Delen via Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Twitter delen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Afdrukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Koptekst dialoogvenster Afdrukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten rechtsboven in het dialoogvenster Afdrukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.PRINT_RANGE </span> </p> </td> 
   <td colname="col2"> <p>Label voor de sectie Pagina's afdrukken selecteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor het keuzerondje "Huidige pagina's". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.PRINT_RANGE_FROM </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor het keuzerondje "Spread range from". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.PRINT_RANGE_TO </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de numerieke kiezer "to". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.PRINT_RANGE_ALL </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor het keuzerondje "Alle pagina's". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.PAGE_HANDLING </span> </p> </td> 
   <td colname="col2"> <p>Label voor de sectie "Paginaverwerking". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor het keuzerondje "1 pagina per vel". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor het keuzerondje "2 pagina's per vel". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Afdrukken.ANNULEREN </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p> De knop Annuleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Bijschrift voor de knop Verzenden naar afdrukken </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Verzenden naar afdrukknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavorietenMenu.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knop Favorieten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>De knop Favoriet toevoegen in de modus Favorieten bewerken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Favoriete knop toevoegen in de normale modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Favorieten verwijderen in de modus Favorieten bewerken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>"Verwijder favoriet"knoop in normale wijze. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>De knop Alle favorieten weergeven wanneer de weergave Favorieten actief is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>De knop Alle favorieten weergeven wanneer de weergave Favorieten inactief is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Favorieten-effect.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Eén favoriet pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY] </span> </p> </td> 
   <td colname="col2"> <p>Paginalabel die door de viewer tijdens het laden wordt gegenereerd. </p> <p>De naam van dat symbool is een sjabloon, waarbij <span class="codeph"> XX een op nul gebaseerde spread-index </span> is in liggende richting en optioneel <span class="codeph"> YY </span> een op nul gebaseerde pagina-index is binnen de spread die wordt bedoeld door <span class="codeph"> XX </span>. </p> <p>alleen van toepassing op het oorspronkelijk geladen element; genegeerd als een element wordt gewijzigd via de <span class="codeph"> API-aanroep setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM </span> </p> </td> 
   <td colname="col2"> <p> Teken dat als scheidingsteken voor paginalabels wordt gebruikt voor het geval labels worden gedefinieerd voor de linker- en rechterpagina in een spread. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>De hoofdbesturingsbalk schuift naar links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Hoofdbesturingsbalk schuift naar rechts. </p> </td> 
  </tr> 
 </tbody> 
</table>

