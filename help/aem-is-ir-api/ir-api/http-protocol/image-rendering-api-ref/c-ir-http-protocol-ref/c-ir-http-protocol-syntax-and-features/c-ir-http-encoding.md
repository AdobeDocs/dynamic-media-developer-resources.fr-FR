---
description: Les valeurs de commande doivent être codées au format http à l'aide des séquences d'échappement %xx, de sorte que les chaînes de valeur n'incluent pas les caractères réservés '=', '&' et '%'.
solution: Experience Manager
title: Codage HTTP de rendu d’image
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# Encodage HTTP de rendu d’image {#image-rendering-http-encoding}

Les valeurs de commande doivent être codées au format http à l&#39;aide des séquences d&#39;échappement %xx, de sorte que les chaînes de valeur n&#39;incluent pas les caractères réservés &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39;.

Sinon, les règles de codage HTTP standard s’appliquent. La spécification HTTP requiert le codage des caractères non sécurisés tels que &#39; (espace), &#39;&quot;&#39; (guillemet-doublon), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; et &#39;>&#39;, ainsi que des caractères de contrôle tels que `<return>` et `<tab>`.

**Attention : Les accolades** Curly { } utilisées comme délimiteurs d’imbrication de requête ne doivent pas être codées. Certains clients de messagerie encodent malheureusement des accolades dans une requête HTTP incorporée. S’il s’agit d’un problème, le rendu d’image permet l’utilisation de parenthèses ( ) plutôt que d’accolades.

## Exemple {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Le fragment de requête ci-dessus doit être codé comme suit :

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Voir aussi {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Spécification HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
