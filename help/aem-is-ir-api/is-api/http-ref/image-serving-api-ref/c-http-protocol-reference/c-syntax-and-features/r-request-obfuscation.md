---
description: Le contenu de l’ensemble des modificateurs d’une partie de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué en appliquant un codage base64 standard.
solution: Experience Manager
title: Obfuscation de requête
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
TQID: 'https://experienceleague.adobe.com/77Q5rV3cP4KoBz3rFKlEmBlumS0TBthuLbLQBETPitE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# Obfuscation de requête{#request-obfuscation}

Le contenu de l’ensemble des modificateurs d’une partie de la chaîne de requête, y compris le suffixe de verrouillage facultatif, peut être masqué en appliquant un codage base64 standard.

Le serveur tente de décoder si `attribute::RequestObfuscation` est défini. Si le décodage échoue, la requête est rejetée. Si le verrouillage de la requête et l’obscurcissement de la requête sont appliqués, le suffixe de verrouillage doit être généré et ajouté avant le codage base64.

>[!IMPORTANT]
>
>Si vous activez cette fonctionnalité, gardez à l’esprit que certaines limitations de son utilisation incluent : <br>- L’interface utilisateur de Dynamic Media peut ne pas afficher les détails corrects pour le champ **[!UICONTROL Dernière publication]**. Cependant, cet effet n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion vidéo en continu HLS ne fonctionne pas lorsque **[!UICONTROL Demander l’obscurcissement]** et **[!UICONTROL Verrouillage des requêtes]** sont activés.<br>- Actuellement, certaines visionneuses Dynamic Media ne fonctionnent pas lorsque **[!UICONTROL Demander l’obscurcissement]** et **[!UICONTROL Verrouillage des requêtes]** sont activées.

## Exemple {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

encode en :

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Toute occurrence de &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39; dans les chaînes de valeur doit être placée dans une séquence d’échappement à l’aide de l’encodage &#39;%xx&#39;, avant que la requête ne soit obfusquée. Il n’est pas nécessaire de coder par http les parties *modificateurs* de la requête avant ou après l’obfuscation, même si le verrouillage de la requête est appliqué, car le codage base64 est sûr pour la transmission par http.

## Voir aussi {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Encodage HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Verrouillage de requête](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
