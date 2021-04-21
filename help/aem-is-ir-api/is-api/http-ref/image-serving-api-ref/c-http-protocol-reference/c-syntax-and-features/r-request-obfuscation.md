---
description: Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué par l'application d'un codage standard base64.
solution: Experience Manager
title: Obscurcissement de demande
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 1%

---


# Obscurcissement de la demande{#request-obfuscation}

Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué par l&#39;application d&#39;un codage standard base64.

Le serveur tente de décoder si `attribute::RequestObfuscation` est défini. Si le décodage échoue, la demande est rejetée. Si le verrouillage des requêtes et l’obscurcissement des requêtes sont appliqués, le suffixe de verrouillage doit être généré et ajouté avant le codage base64.

>[!IMPORTANT]
>
>Si vous activez cette fonction, sachez qu’il existe certaines limitations à son utilisation, notamment :<br>- L’interface utilisateur de Dynamic Media peut ne pas afficher les détails corrects pour le champ **[!UICONTROL Dernière publication]**. Cependant, cela n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion en flux continu de vidéos HLS ne fonctionne pas lorsque l’option **[!UICONTROL Demander l’obscurcissement et le verrouillage de la]**   **** requête sont activés.<br>- Actuellement, certaines visionneuses Dynamic Media ne fonctionnent pas lorsque l’option  **[!UICONTROL Obscurcissement des]** requêtes et  **[!UICONTROL verrouillage des]** requêtes est activée.

## Exemple {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

code à :

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Les occurrences de &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39; dans les chaînes de valeur doivent être ignorées à l&#39;aide de l&#39;encodage &#39;%xx&#39;, avant que la requête ne soit obscurcie. Il n&#39;est pas nécessaire d&#39;encoder autrement la partie *modificateurs* de la requête avant ou après l&#39;obscurcissement, même si le verrouillage de la requête est appliqué, puisque l&#39;encodage base64 est sûr pour la transmission http.

## Voir aussi {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Encodage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP, Verrouillage [ de ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)requête,  [attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
