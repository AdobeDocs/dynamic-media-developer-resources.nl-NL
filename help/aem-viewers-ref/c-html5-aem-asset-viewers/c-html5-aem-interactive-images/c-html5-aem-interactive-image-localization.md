---
description: Bepaalde inhoud die in de Interactive Image Viewer wordt weergegeven, is afhankelijk van lokalisatie. Dit omvat knopinfo voor gebruikersinterface-elementen en een informatiebericht dat tijdens het laden wordt weergegeven in de zoomweergave voor vervolgmenu's.
seo-description: Bepaalde inhoud die in de Interactive Image Viewer wordt weergegeven, is afhankelijk van lokalisatie. Dit omvat knopinfo voor gebruikersinterface-elementen en een informatiebericht dat tijdens het laden wordt weergegeven in de zoomweergave voor vervolgmenu's.
seo-title: Lokalisatie van gebruikersinterface-elementen
title: Lokalisatie van gebruikersinterface-elementen
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de Interactive Image Viewer wordt weergegeven, is afhankelijk van lokalisatie. Dit omvat knopinfo voor gebruikersinterface-elementen en een informatiebericht dat tijdens het laden wordt weergegeven in de zoomweergave voor vervolgmenu&#39;s.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door de speciale Viewer SDK-id SYMBOL. Aan elk SYMBOL is een standaardtekstwaarde gekoppeld voor een Engelse landinstelling ( `"en"`) die wordt geleverd met de viewer buiten het vak. Bovendien kunnen er door de gebruiker gedefinieerde waarden worden ingesteld voor zoveel landinstellingen als nodig is.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te controleren of er voor elke ondersteunde SYMBOL-landinstelling een door de gebruiker gedefinieerde waarde is. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Dit object bevat een lijst met ondersteunde landinstellingen, SYMBOL-tekstwaarden voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject is het volgende:

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
}, 
defaultLocale:"en" 
}
```

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt het lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De webpaginacode moet het lokalisatieobject doorgeven aan de viewerconstructor als een waarde van het `localizedTexts` veld van het configuratieobject. Een andere optie is om het lokalisatieobject door te geven door `setLocalizedTexts(localizationInfo)` methode aan te roepen.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-label voor viewerelement op hoofdniveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rolbeschrijving voor hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
 </tbody> 
</table>

