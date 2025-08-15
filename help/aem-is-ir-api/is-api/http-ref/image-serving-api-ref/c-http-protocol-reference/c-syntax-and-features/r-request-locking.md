---
description: Afin de réduire les possibilités de manipulation des demandes, une simple fonction de verrouillage est fournie.
solution: Experience Manager
title: Verrouillage de requête
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Verrouillage de requête{#request-locking}

Afin de réduire les possibilités de manipulation des demandes, une simple fonction de verrouillage est fournie.

Si attribute::RequestLock est défini, une valeur de verrouillage doit être ajoutée à la requête, sous la forme d’un `&xxxx`, xxxx étant une valeur hexadécimale à quatre chiffres. Cette valeur hex est générée à l’aide d’un simple algorithme de hachage appliqué à la partie *modificateurs* de la requête (après le « ? ») qui sépare le chemin de l’URL des *modificateurs*). Cette opération doit être effectuée après l’encodage complet de la requête http, mais avant son obscurcissement (facultatif). Après avoir supprimé l’obscurcissement de la requête, le serveur utilise le même algorithme de hachage sur la chaîne de modificateur (à l’exclusion des 5 derniers caractères, qui contiennent la valeur de verrouillage). Si la clé générée ne correspond pas au verrou, la requête est rejetée.

>[!IMPORTANT]
>
>Si vous activez cette fonctionnalité, gardez à l’esprit que certaines limitations de son utilisation incluent : <br>- L’interface utilisateur de Dynamic Media peut ne pas afficher les détails corrects pour le champ **[!UICONTROL Dernière publication]**. Toutefois, cet impact n’a aucune incidence sur la publication.<br>- Actuellement, la diffusion vidéo en continu HLS ne fonctionne pas lorsque **[!UICONTROL Demander l’obscurcissement]** et **[!UICONTROL Demander le verrouillage]** sont activés.<br>- Actuellement, certaines visionneuses Dynamic Media ne fonctionnent pas lorsque les options **[!UICONTROL Obfuscation de requête]** et **[!UICONTROL Verrouillage de requête]** sont activées.

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

[Encodage HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Obscurcissement de requête](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
