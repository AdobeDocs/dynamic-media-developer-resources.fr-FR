---
description: Afin de réduire les possibilités de falsification des requêtes, un système de verrouillage simple est fourni.
seo-description: Afin de réduire les possibilités de falsification des requêtes, un système de verrouillage simple est fourni.
seo-title: Demander le verrouillage
solution: Experience Manager
title: Demander le verrouillage
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Request locking{#request-locking}

Afin de réduire les possibilités de falsification des requêtes, un système de verrouillage simple est fourni.

Si attribut::RequestLock est défini, une valeur de verrouillage doit être ajoutée à la requête, sous forme de `&xxxx`valeur, avec xxxx comme valeur hexadécimale à quatre chiffres. Cette valeur hexadécimale est générée à l’aide d’un algorithme de hachage simple appliqué à la partie *modificateurs* de la requête (après le &quot;?&quot;). qui sépare le chemin d’accès à l’URL des *modificateurs*). Cette opération doit être effectuée une fois que la requête est entièrement codée en http, mais avant qu’elle ne soit (éventuellement) obscurcie. Après avoir démasqué la requête, le serveur utilisera le même algorithme de hachage sur la chaîne de modificateur (à l’exception des 5 derniers caractères qui contiennent la valeur de verrouillage). Si la clé générée ne correspond pas au verrou, la demande est rejetée.

>[!IMPORTANT]
>
>Si vous activez cette fonction, sachez qu’il existe certaines restrictions à son utilisation, notamment les suivantes :<br>- L’interface utilisateur Contenu multimédia dynamique peut ne pas afficher les détails corrects pour le champ **[!UICONTROL Dernière publication]** . Cependant, cela n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion vidéo en flux continu HLS ne fonctionne pas lorsque l’obscurcissement **[!UICONTROL de]** requête et le verrouillage **[!UICONTROL de]** requête sont activés.<br>- Actuellement, certaines visionneuses de médias dynamiques ne fonctionnent pas lorsque l’obscurcissement **[!UICONTROL des]** requêtes et le verrouillage **[!UICONTROL des]** requêtes sont activés.

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

[Encodage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)HTTP, Obscurcissement [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)requête, [attribut ::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
