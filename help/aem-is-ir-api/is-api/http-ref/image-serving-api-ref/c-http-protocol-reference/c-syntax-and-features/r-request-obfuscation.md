---
description: Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué par l’application du codage standard base64.
seo-description: Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué par l’application du codage standard base64.
seo-title: Obscurcissement de demande
solution: Experience Manager
title: Obscurcissement de demande
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Request obfuscation{#request-obfuscation}

Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué par l’application du codage standard base64.

Le serveur tente de décoder si `attribute::RequestObfuscation` est défini. Si le décodage échoue, la requête est rejetée. Si le verrouillage des requêtes et l’obscurcissement des requêtes sont appliqués, le suffixe de verrouillage doit être généré et ajouté avant le codage base64.

## Exemple {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

code à :

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Les occurrences de &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39; dans les chaînes de valeur doivent être ignorées à l&#39;aide du codage &#39;%xx&#39;, avant que la requête ne soit obscurcie. Il n’est pas nécessaire d’encoder autrement http-encode la partie *modificateurs* de la requête avant ou après l’obscurcissement, même si le verrouillage de la requête est appliqué, puisque le codage base64 est sûr pour la transmission http.

## Voir aussi {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Encodage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)HTTP, Verrouillage [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)requête, [attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
