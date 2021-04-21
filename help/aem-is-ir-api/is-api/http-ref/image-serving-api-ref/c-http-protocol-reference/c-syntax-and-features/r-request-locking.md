---
description: Afin de réduire les possibilités de falsification des requêtes, un système de verrouillage simple est fourni.
solution: Experience Manager
title: Demander le verrouillage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Demander le verrouillage{#request-locking}

Afin de réduire les possibilités de falsification des requêtes, un système de verrouillage simple est fourni.

Si attribut::RequestLock est défini, une valeur de verrouillage doit être ajoutée à la requête, sous la forme `&xxxx`, avec xxxx comme valeur hexadécimale à quatre chiffres. Cette valeur hexadécimale est générée à l’aide d’un algorithme de hachage simple appliqué à la partie *modificateurs* de la requête (après le &quot;?&quot; qui sépare le chemin d’accès à l’URL des modificateurs **). Cette opération doit être effectuée une fois que la requête est entièrement codée en http, mais avant qu’elle ne soit (éventuellement) obscurcie. Après avoir démasqué la requête, le serveur utilisera le même algorithme de hachage sur la chaîne de modificateur (à l’exception des 5 derniers caractères qui contiennent la valeur de verrouillage). Si la clé générée ne correspond pas au verrou, la demande est rejetée.

>[!IMPORTANT]
>
>Si vous activez cette fonction, sachez qu’il existe certaines limitations à son utilisation, notamment :<br>- L’interface utilisateur de Dynamic Media peut ne pas afficher les détails corrects pour le champ **[!UICONTROL Dernière publication]**. Cependant, cela n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion en flux continu de vidéos HLS ne fonctionne pas lorsque l’option **[!UICONTROL Demander l’obscurcissement et le verrouillage de la]**   **** requête sont activés.<br>- Actuellement, certaines visionneuses Dynamic Media ne fonctionnent pas lorsque l’option  **[!UICONTROL Obscurcissement des]** requêtes et  **[!UICONTROL verrouillage des]** requêtes est activée.

Exemple de code C++ pour générer la valeur de verrouillage de la demande :

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

[Encodage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP, Obscurcissement [ de ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)requête,  [attribut ::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
