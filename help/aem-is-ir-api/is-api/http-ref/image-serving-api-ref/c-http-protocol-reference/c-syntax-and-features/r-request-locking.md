---
description: Afin de réduire les possibilités de falsification des demandes, une installation de verrouillage simple est fournie.
seo-description: Afin de réduire les possibilités de falsification des demandes, une installation de verrouillage simple est fournie.
seo-title: Demander le verrouillage
solution: Experience Manager
title: Demander le verrouillage
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Request locking{#request-locking}

Afin de réduire les possibilités de falsification des demandes, une installation de verrouillage simple est fournie.

Si attribute::RequestLock est défini, une valeur de verrouillage doit être ajoutée à la requête, sous la forme `&xxxx`, avec xxxx comme valeur hexadécimale à quatre chiffres. Cette valeur hexadécimale est générée à l’aide d’un algorithme de hachage simple appliqué à la partie *modificateurs* de la requête (après le &quot;?&quot;). qui sépare le chemin de l’URL des *modificateurs*). Cette opération doit être effectuée une fois que la requête est entièrement codée en http, mais avant qu’elle ne soit (éventuellement) obscurcie. Après avoir démasqué la requête, le serveur utilisera le même algorithme de hachage sur la chaîne de modificateur (à l’exclusion des 5 derniers caractères qui contiennent la valeur de verrouillage). Si la clé générée ne correspond pas au verrou, la requête est rejetée.

Exemple de code C++ pour générer la valeur de verrouillage de requête :

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Voir aussi {#section-a6d45406c0354669ac581793e4fa8436}

[Encodage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)HTTP, Obscurcissement [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)requête, [attribut::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
