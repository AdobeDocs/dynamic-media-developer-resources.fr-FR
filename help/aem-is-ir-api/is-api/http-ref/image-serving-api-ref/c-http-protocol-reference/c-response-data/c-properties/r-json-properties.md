---
description: Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), encapsulées dans un appel de fonction JavaScript.
seo-description: Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), encapsulées dans un appel de fonction JavaScript.
seo-title: Propriétés JSONP
solution: Experience Manager
title: Propriétés JSONP
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Propriétés JSONP{#jsonp-properties}

Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), encapsulées dans un appel de fonction JavaScript.

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

La fonction `s7jsonResponse` JavaScript doit être définie par le client. Dans sa forme la plus simple, la fonction peut se présenter comme suit :

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Default is `s7jsonResponse`.

Le pack des visionneuses Scene7 Image Serving comprend un utilitaire permettant de demander et d’analyser des données au format JSONP à partir de la diffusion d’images.

Voir [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) pour plus d’informations sur le format JSONP.

Voir [www.json.org](http://www.json.org) pour plus d’informations sur le format JSON.

Voir aussi [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
