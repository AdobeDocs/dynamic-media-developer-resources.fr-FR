---
title: Rendu d’image Encodage HTTP
description: Les valeurs de commande doivent être codées en http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés '=', '&' et ' %'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# Rendu d’image Encodage HTTP{#image-rendering-http-encoding}

Les valeurs de commande doivent être codées en http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés &#39;=&#39;, &#39;&amp;&#39; et &#39; %&#39;.

Dans le cas contraire, les règles de codage HTTP standard s’appliquent. La spécification HTTP exige le codage des caractères dangereux tels que &#39; &#39; (espace), &#39;&quot;&#39;(guillemet double), &#39;#&#39;, &#39; %&#39;, &#39;&#39;, ainsi &lt;&#39;, and=&quot;&quot; &#39;=&quot;&quot;>que des caractères de contrôle, tels que `<return>` et `<tab>`.&lt;/&#39;,>

**Attention :** les accolades { } utilisées comme délimiteurs d’imbrication de requête ne doivent pas être codées. Malheureusement, certains clients de messagerie encodent des accolades dans les requêtes HTTP intégrées. Si ce problème pose problème, Image Rendering autorise l’utilisation de parenthèses ( ) au lieu d’accolades.

## Exemple {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Le fragment de requête ci-dessus doit être codé comme suit :

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Voir aussi {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Spécification HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
