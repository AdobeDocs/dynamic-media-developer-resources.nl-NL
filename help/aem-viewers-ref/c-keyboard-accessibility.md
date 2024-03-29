---
title: Toetsenbordtoegankelijkheid en -navigatie
description: Alle functies die beschikbaar worden gesteld in de viewerinterface Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Dimensional (3D), Carousel, Interactive Image, Interactive Video, en Video360 zijn toegankelijk via het toetsenbord.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Toetsenbordtoegankelijkheid en -navigatie{#keyboard-accessibility-and-navigation}

Alle functies die beschikbaar worden gesteld in de viewerinterface Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carousel, Dimensional (3D), Interactive Image, Interactive Video, en Video360 zijn toegankelijk via het toetsenbord.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Toetsenbordtoegankelijkheid en -navigatie {#topic-f5650e9493404e55a3627c8d1366b861}

Alle functies die beschikbaar worden gesteld in de viewerinterface Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carousel, Dimensional (3D), Interactive Image, Interactive Video, en Video360 zijn toegankelijk via het toetsenbord.

Een eindgebruiker kan met behulp van **[!UICONTROL Tab]** en **[!UICONTROL Shift+Tab]** toetsaanslagen. Gebruiken **[!UICONTROL Tab]** gaat de invoerfocus naar het volgende interface-element in de tabvolgorde; gebruiken **[!UICONTROL Shift+Tab]** Hiermee wordt invoerfocus teruggezet naar het vorige gebruikersinterface-element. Het focustraversal volgt de natuurlijke locatie van het interface-element op het scherm en beweegt van links naar rechts en vervolgens van boven naar beneden.

Afhankelijk van het besturingssysteem en de instellingen van de webbrowser ontvangt het interface-element met invoerfocus een visuele focusindicatie. De visuele indicator kan bijvoorbeeld een dunne rand zijn die rondom het interface-element wordt weergegeven.

Het is mogelijk een dergelijke focusmarkering uit te schakelen of aan te passen in de CSS van de viewer. Klik in de inhoudsopgave van dit Help-systeem onder een specifieke viewernaam (bijvoorbeeld Standaardzoom of Interactieve video) op **Aanpassen *naam van viewer*** >** Focus markeren **.

Toetsen die door afzonderlijke gebruikersinterface-elementen van de viewer worden ondersteund, zijn meestal duidelijk en gemakkelijk te vinden.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Handeling </p> </th> 
   <th colname="col2" class="entry"> <p>Toetsaanslag </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Knopcomponenten activeren </p> </td> 
   <td colname="col2"> <p>Spatiebalk of Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In- of uitzoomen </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> of <span class="uicontrol"> - </span>, respectievelijk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoomen opnieuw instellen </p> </td> 
   <td colname="col2"> <p>Esc-toets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pannen </p> </td> 
   <td colname="col2"> <p>Pijl-omhoog, omlaag, links of rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een afbeelding van 360 graden draaien </p> </td> 
   <td colname="col2"> <p>Gebruik de pijltoetsen wanneer de afbeelding opnieuw wordt ingesteld. </p> <p>Gebruik de pijltoets omhoog of omlaag wanneer u werkt met multidimensionale centrifuges. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Staalselectie van product </p> </td> 
   <td colname="col2"> <p>Pijl-omhoog, -omlaag, -links of -rechts; Home- of End-toets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Productstaalactivering </p> </td> 
   <td colname="col2"> <p>Spatiebalk of Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video en interactieve video, geleidelijk terugspoelen </p> </td> 
   <td colname="col2"> <p>Pijltoets links of omhoog. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video en interactieve video, snel vooruit </p> </td> 
   <td colname="col2"> <p>Pijl-rechts of Pijl-omlaag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video en interactieve video, ga naar begin of eind </p> </td> 
   <td colname="col2"> <p>Home- of End-toets respectievelijk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video en Interactieve video, volumeniveau bepalen wanneer de focus op de schuifregelaar is </p> </td> 
   <td colname="col2"> <p>Pijl-omhoog, -omlaag, -links of -rechts; Home- of End-toets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video en interactieve video, veranderbaar volume </p> </td> 
   <td colname="col2"> <p>Met de toetsen Pijl, Home en End kunt u het volumeniveau bepalen wanneer de focus zich op het schuifregelaargedeelte bevindt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video, wanneer modaal dialoogvenster wordt weergegeven, wordt focustraversal beperkt tot besturingselementen voor dialoogvensters. </p> </td> 
   <td colname="col2"> <p>Esc-toets om het dialoogvenster te sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, bannerafbeelding wijzigen in hoofdweergave </p> </td> 
   <td colname="col2"> <p>Pijl-links of Pijl-rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, hotspot selectie en hotspot activering </p> </td> 
   <td colname="col2"> <p>Selectie hotspot: pijl-omhoog, pijl-omlaag, pijl-links of pijl-rechts </p> <p>Hotspot activeren: Spatiebalk of Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, verander het paginabeeld in de belangrijkste mening </p> </td> 
   <td colname="col2"> <p> Pijltoetsen links of rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, miniatuurselectie </p> </td> 
   <td colname="col2"> <p>Pijltoetsen; Home en End. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, staalactivering </p> </td> 
   <td colname="col2"> <p>Spatiebalk of Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, hotspot selecteren </p> </td> 
   <td colname="col2"> <p>Pijltoetsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, activering </p> </td> 
   <td colname="col2"> <p>Spatie- of Enter-toetsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, drop-down componenten activeren </p> </td> 
   <td colname="col2"> <p> Pijltoets-omlaag; Spatie of Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, wanneer focus zich in dropdropdeelvenster bevindt </p> </td> 
   <td colname="col2"> <p>Gebruik de pijltoetsen om een specifiek item in het deelvenster te selecteren voordat u het activeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In eCatalog geldt dat wanneer een modaal dialoogvenster wordt weergegeven, focustraversal alleen geldt voor besturingselementen in dialoogvensters. </p> </td> 
   <td colname="col2"> <p>Esc-toets om het dialoogvenster te sluiten. </p> </td> 
  </tr> 
 </tbody> 
</table>
