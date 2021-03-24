---
description: Vervangende variabele wordt gebruikt om waarden van het verzoekURL naar FXG malplaatjes over te brengen die op de server worden opgeslagen.
solution: Experience Manager
title: Substitutievariabelen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Vervangende variabelen{#substitution-variables}

Vervangende variabele wordt gebruikt om waarden van het verzoekURL naar FXG malplaatjes over te brengen die op de server worden opgeslagen.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Naam variabele. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Waarde waarop de variabele moet worden ingesteld (tekenreeks). </p> </td> 
 </tr> 
</table>

* Variabelendefinities en -verwijzingen kunnen voorkomen in het querygedeelte van de aanvraag-URL.
* Variabelen worden gedefinieerd als hierboven, vergelijkbaar met andere IS-opdrachten; de regelafstand &#39;$&#39; geeft de opdracht aan als een variabele definitie.
* De variabelenaam `*`var`*` is hoofdlettergevoelig en kan bestaan uit een willekeurige combinatie van letters, cijfers, &#39;-&#39; en &#39;_&#39;.
* Belangrijke waarde moet URL-gecodeerd zijn met één controle voor veilige HTTP-verzending.

