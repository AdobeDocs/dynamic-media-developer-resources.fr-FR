---
title: Encodage HTTP de rendu d’image
description: Les valeurs de commande doivent être codées au format http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés '=', '&' et '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# Encodage HTTP de rendu d’image{#image-rendering-http-encoding}

Les valeurs de commande doivent être codées au format http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39;.

Dans le cas contraire, les règles de codage HTTP standard s’appliquent. La spécification HTTP nécessite le codage de caractères non sûrs tels que &#39; (espace), &#39;&quot;&#39; (guillemet double), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; et &#39;>&#39;, ainsi que des caractères de contrôle, tels que `<return>` et `<tab>`.

**Attention :** Les accolades { } utilisées comme délimiteurs d’imbrication de requête ne doivent pas être codées. Certains clients de messagerie codent malheureusement des accolades dans une requête HTTP incorporée. Si ce problème se produit, le rendu d’image permet l’utilisation de parenthèses ( ) au lieu d’accolades.

## Exemple {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Le fragment de requête ci-dessus doit être codé comme suit :

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Voir aussi {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Spécification HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
