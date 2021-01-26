---
description: Vervangende variabele wordt gebruikt om waarden van het verzoekURL naar FXG malplaatjes over te brengen die op de server worden opgeslagen.
seo-description: Vervangende variabele wordt gebruikt om waarden van het verzoekURL naar FXG malplaatjes over te brengen die op de server worden opgeslagen.
seo-title: Substitutievariabelen
solution: Experience Manager
title: Substitutievariabelen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
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

