---
description: Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être obscurci par l’application d’un codage base64 standard.
solution: Experience Manager
title: Obscurcissement de requête
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# Obscurcissement de requête{#request-obfuscation}

Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être obscurci par l’application d’un codage base64 standard.

Le serveur tente de décoder si `attribute::RequestObfuscation` est défini. Si le décodage échoue, la requête est rejetée. Si le verrouillage des requêtes et l’obscurcissement des requêtes sont appliqués, le suffixe de verrouillage doit être généré et ajouté avant le codage base64.

>[!IMPORTANT]
>
>Si vous activez cette fonction, sachez qu’il existe certaines limites à son utilisation qui incluent les éléments suivants :<br>- L’interface utilisateur de Dynamic Media peut ne pas afficher les détails corrects pour le champ **[!UICONTROL Dernière publication]**. Toutefois, cet impact n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion vidéo HLS en flux continu ne fonctionne pas lorsque l’**[!UICONTROL obscurcissement des]** requêtes et le verrouillage des  **[!UICONTROL requêtes sont activés.]** <br>- Actuellement, certaines visionneuses Dynamic Media ne fonctionnent pas lorsque l’ **[!UICONTROL obscurcissement des]** requêtes et le verrouillage des  **[!UICONTROL requêtes]** sont activés.

## Exemple {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

code à :

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Les occurrences de &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39; dans les chaînes de valeur doivent être placées dans une séquence d’échappement à l’aide de l’encodage &#39;%xx&#39;, avant que la requête ne soit obscurcie. Il n’est pas nécessaire de coder autrement http-encode la partie *modificateurs* de la requête avant ou après l’obscurcissement, même si le verrouillage de la requête est appliqué, puisque l’encodage base64 est sécurisé pour la transmission http.

## Voir aussi {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Encodage HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Verrouillage de requête](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
