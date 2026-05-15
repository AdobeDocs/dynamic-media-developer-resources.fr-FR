---
title: Propriétés JSONP
description: Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), enveloppées dans un appel de fonction JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: 'https://experienceleague.adobe.com/pMirwhZ5n0mVuK2If4kJz3XDQZPDhORJCZBLsDf2C8I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Propriétés JSONP{#jsonp-properties}

Si jsonp est spécifié comme format de réponse, les données de réponse sont formatées à l’aide de JSONP (JavaScript Object Notation with Padding), enveloppées dans un appel de fonction JavaScript.

Le client peut spécifier un identifiant de requête unique facultatif ( *`reqId`*), qui est renvoyé dans la réponse et permet au client de distinguer les réponses multiples reçues de manière asynchrone. Une réponse type possède la structure générale suivante :

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

La fonction `s7jsonResponse` JavaScript doit être définie par le client. Dans sa forme la plus simple, la fonction peut ressembler à ceci :

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue `req=` paramètre :

`req=...,json [&handler = reqHandler]`

La syntaxe `<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

Le package Visionneuses d’images de diffusion Dynamic Media comprend un utilitaire permettant de demander et d’analyser les données au format JSONP de la diffusion d’images.

Voir [&#128279;](https://en.wikipedia.org/wiki/JSONP) pour plus d’informations sur le format JSONP.

Voir [&#128279;](https://www.json.org/json-en.html) pour plus d’informations sur le format JSON.

Voir aussi [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
