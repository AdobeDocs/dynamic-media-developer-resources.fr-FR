---
title: Encodage HTTP de rendu d’image
description: Les valeurs de commande doivent être encodées en http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés « = », «& » et «% ».
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
TQID: 'https://experienceleague.adobe.com/TNB9NbrGzMGS64CxHgj7aXlSHz8-KPBB0hMxB36mKvI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# Encodage HTTP de rendu d’image{#image-rendering-http-encoding}

Les valeurs de commande doivent être encodées en http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés « = », «&amp; » et «% ».

Dans le cas contraire, les règles de codage HTTP standard s’appliquent. La spécification HTTP nécessite le codage des caractères non sécurisés tels que &#39; &#39; (espace), &#39;« &#39; (guillemet double), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; et &#39;>&#39;, ainsi que des caractères de contrôle, tels que `<return>` et `<tab>`.

**Attention :** les accolades { } utilisées comme délimiteurs d’imbrication de requête ne doivent pas être codées. Certains clients de messagerie codent malheureusement des accolades dans des requêtes HTTP incorporées. Si ce problème se pose, le rendu d’image permet l’utilisation de parenthèses ( ) au lieu d’accolades.

## Exemple {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Le fragment de requête ci-dessus doit être codé comme suit :

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Voir aussi {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Spécification HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)

