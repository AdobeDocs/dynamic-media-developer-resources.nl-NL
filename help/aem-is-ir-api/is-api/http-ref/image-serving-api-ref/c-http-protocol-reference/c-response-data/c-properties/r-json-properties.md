---
title: JSONP-eigenschappen
description: Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# JSONP-eigenschappen{#jsonp-properties}

Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.

De client kan een optionele unieke aanvraag-id opgeven ( *`reqId`*), dat in de reactie wordt geretourneerd en de client in staat stelt meerdere ontvangen reacties asynchroon te onderscheiden. Een typische reactie heeft de volgende algemene structuur:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

De `s7jsonResponse` JavaScript-functie moet door de client worden gedefinieerd. In zijn eenvoudigste vorm kan de functie er als volgt uitzien:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler]`

De `<reqHandler>` syntaxis is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.

Het Dynamic Media Image Serving Viewers-pakket bevat een hulpprogramma voor het aanvragen en parseren van gegevens met de JSONP-indeling van Image Serving.

Zie [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) voor meer informatie over het formaat JSONP.

Zie [www.json.org](https://www.json.org/json-en.html) voor meer informatie over de JSON-indeling.

Zie ook [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
