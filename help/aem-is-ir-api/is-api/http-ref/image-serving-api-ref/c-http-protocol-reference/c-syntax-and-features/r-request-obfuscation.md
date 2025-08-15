---
description: Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué en appliquant un codage standard en base64.
solution: Experience Manager
title: Obscurcissement de requête
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# Obscurcissement de requête{#request-obfuscation}

Le contenu de la partie entière des modificateurs de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué en appliquant un codage standard en base64.

Le serveur tente de décoder si `attribute::RequestObfuscation` est défini. Si le décodage échoue, la requête est rejetée. Si le verrouillage de requête et l’obscurcissement de requête sont appliqués, le suffixe de verrouillage doit être généré et ajouté avant le codage base64.

>[!IMPORTANT]
>
>Si vous activez cette fonctionnalité, sachez qu’il existe certaines limitations à son utilisation qui incluent les suivantes :<br> - L’interface utilisateur Dynamic Media peut ne pas afficher les détails corrects pour le **[!UICONTROL champ Dernière publication]** . Toutefois, cette incidence n’a aucune incidence sur la publication.<br>- Actuellement, le streaming vidéo HLS ne fonctionne pas lorsque **[!UICONTROL l’obscurcissement]** de requête et **[!UICONTROL le verrouillage]** de requête sont activés.<br>- Actuellement, certains visualiseurs Dynamic Media ne fonctionnent pas lorsque **[!UICONTROL l’obscurcissement]** de requête et **[!UICONTROL le verrouillage]** de requête sont activés.

## Exemple {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

code à :

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Toutes les occurrences de &#39;=&#39;, &#39;&amp;&#39; et &#39; %&#39; dans les chaînes de valeur doivent être placées dans une séquence d’échappement à l’aide du codage &#39; %xx&#39;, avant que la requête ne soit obscurcie. Il n’est pas nécessaire d’encoder autrement http-encode la partie modificateurs de la requête avant ou après l’obscurcissement *, même si le verrouillage de* requête est appliqué, car l’encodage base64 est sûr pour la transmission http.

## Voir aussi {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Encodage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP, [verrouillage de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c) requête, [attribut ::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
