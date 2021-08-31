---
description: Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), enveloppées dans un appel de fonction JavaScript.
solution: Experience Manager
title: Propriétés JSONP
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Propriétés JSONP{#jsonp-properties}

Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), enveloppées dans un appel de fonction JavaScript.

Le client peut spécifier un identifiant de requête unique facultatif ( *`reqId`*), qui est renvoyé dans la réponse et permet au client de distinguer plusieurs réponses reçues de manière asynchrone. Une réponse type présente la structure générale suivante :

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

La fonction JavaScript `s7jsonResponse` doit être définie par le client. Dans sa forme la plus simple, la fonction peut se présenter comme suit :

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

Le package Visionneuses Dynamic Media Image Serving comprend un utilitaire permettant de demander et d’analyser des données au format JSONP à partir du serveur d’images.

Voir [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) pour plus d’informations sur le format JSONP.

Voir [www.json.org](https://www.json.org) pour plus d’informations sur le format JSON.

Voir aussi [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
