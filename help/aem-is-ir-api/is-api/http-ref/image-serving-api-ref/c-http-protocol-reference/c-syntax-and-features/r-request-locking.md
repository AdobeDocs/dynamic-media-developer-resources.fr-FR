---
description: Pour réduire les possibilités de traitement des requêtes, une simple fonction de verrouillage est disponible.
solution: Experience Manager
title: Demander le verrouillage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Demander le verrouillage{#request-locking}

Pour réduire les possibilités de traitement des requêtes, une simple fonction de verrouillage est disponible.

Si attribute::RequestLock est défini, une valeur de verrouillage doit être ajoutée à la requête, sous la forme `&xxxx`, xxxx étant une valeur hexadécimale de quatre chiffres. Cette valeur hexadécimale est générée à l’aide d’un algorithme de hachage simple appliqué à la variable *modificateurs* partie de la requête (après le &quot;?&quot; qui sépare le chemin de l’URL du *modificateurs*). Cette opération doit être effectuée une fois que la requête est entièrement codée en HTTP, mais avant qu’elle ne soit (éventuellement) obscurcie. Après avoir démasqué la requête, le serveur utilise le même algorithme de hachage sur la chaîne de modification (à l’exception des 5 derniers caractères, qui contiennent la valeur de verrouillage). Si la clé générée ne correspond pas au verrou, la demande est rejetée.

>[!IMPORTANT]
>
>Si vous activez cette fonction, sachez que son utilisation présente certaines limites, notamment :<br>- Il se peut que l’interface utilisateur de Dynamic Media n’affiche pas les détails corrects pour la variable **[!UICONTROL Dernière publication]** champ . Toutefois, cet impact n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion en continu de vidéos HLS ne fonctionne pas lorsque **[!UICONTROL Obscurcissement de requête]** et **[!UICONTROL Demander le verrouillage]** sont activées.<br>- Actuellement, certaines visionneuses Dynamic Media ne fonctionnent pas lorsque **[!UICONTROL Obscurcissement de requête]** et **[!UICONTROL Demander le verrouillage]** sont activées.

C++ exemple de code pour générer la valeur de verrouillage de requête :

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

[Encodage HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Obscurcissement de requête](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
