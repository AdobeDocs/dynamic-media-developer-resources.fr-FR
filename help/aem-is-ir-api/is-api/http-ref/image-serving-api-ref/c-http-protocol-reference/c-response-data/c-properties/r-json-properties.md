---
title: Propriétés JSONP
description: Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), enveloppé dans un appel de fonction JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Propriétés JSONP{#jsonp-properties}

Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), enveloppé dans un appel de fonction JavaScript.

Le client peut spécifier un identificateur de demande unique facultatif ( *`reqId`*), qui est renvoyé dans la réponse et lui permet de distinguer plusieurs réponses reçues de manière asynchrone. Une réponse typique présente la structure générale suivante :

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

La `s7jsonResponse` fonction JavaScript doit être définie par le client. Dans sa forme la plus simple, la fonction pourrait ressembler à ceci :

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Les demandes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler]`

La `<reqHandler>` syntaxe correspond au nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.

Le package Dynamic Media Image Serving Viewers inclut un utilitaire permettant de demander et d’analyser les données au format JSONP à partir du serveur d’images.

Pour plus d’informations sur le format JSONP, voir [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) .

Pour plus d’informations sur le format JSON, voir [www.json.org](https://www.json.org/json-en.html) .

Voir aussi [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
