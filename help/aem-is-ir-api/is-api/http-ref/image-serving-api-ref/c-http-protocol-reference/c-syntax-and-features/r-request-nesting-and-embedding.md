---
description: La diffusion d’images prend en charge l’imbrication illimitée des requêtes de diffusion d’images, l’incorporation des requêtes de rendu d’images et l’incorporation des images récupérées de serveurs étrangers. Seules les images de calque et les masques de calque prennent en charge ces mécanismes.
solution: Experience Manager
title: Demander l’imbrication et l’incorporation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
TQID: 'https://experienceleague.adobe.com/qDQJjs8DvL7C11yBFGaHdC43HhRTTeTyVUOyBbWuSJA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1061
ht-degree: 0%

---

# Demander l’imbrication et l’incorporation{#request-nesting-and-embedding}

La diffusion d’images prend en charge l’imbrication illimitée des requêtes de diffusion d’images, l’incorporation des requêtes de rendu d’images et l’incorporation des images récupérées de serveurs étrangers. Seules les images de calque et les masques de calque prennent en charge ces mécanismes.

>[!NOTE]
>
>Certains clients de messagerie et serveurs proxy peuvent coder les accolades utilisées pour la syntaxe d’imbrication et d’incorporation. Les applications pour lesquelles ce problème se produit doivent utiliser des parenthèses plutôt que des accolades.

## Requêtes de diffusion d’images imbriquées {#section-6954202119e0466f8ff27c79f4f039c8}

Une requête entière de diffusion d’images peut être utilisée en tant que source de calque en la spécifiant dans la commande `src=` (ou `mask=`) à l’aide de la syntaxe suivante :

`…&src=is( nestedRequest)&…`

Le jeton `is` respecte la casse.

La requête imbriquée ne doit pas inclure le chemin racine du serveur (généralement ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En fait, les requêtes imbriquées doivent être codées de la même manière que la requête externe (imbriquée).

Les règles de prétraitement sont appliquées aux requêtes imbriquées.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de la requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Si l’image de résultat des requêtes imbriquées inclut des données de masque (alpha), elle est transmise au calque d’incorporation en tant que masque de calque.

Les `attribute::MaxPix` et `attribute::DefaultPix` du catalogue d’images qui s’appliquent à la requête imbriquée sont également ignorés.

Le résultat de l’image d’une requête IMS imbriquée peut être mis en cache en incluant éventuellement `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Requêtes de rendu d’image incorporées {#section-69c5548db930412b9b90d9b2951a6969}

Lorsque le rendu d’image Dynamic Media est activé sur le serveur, les requêtes de rendu peuvent être utilisées comme sources de calque en les spécifiant dans la commande src= (ou mask=). Utilisez la syntaxe suivante :

` …&src=ir( *[!DNL renderRequest]*)&…`

Le jeton `ir` respecte la casse.

*[!DNL renderRequest]* est la requête de rendu d’image habituelle, à l’exclusion du chemin racine HTTP ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes de rendu d’image suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Les `attribute::MaxPix` et `attribute::DefaultPix` du catalogue de matières qui s’appliquent à la requête de rendu imbriquée sont également ignorés.

Le résultat de l’image d’une requête infrarouge imbriquée peut être mis en cache en incluant éventuellement `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Requêtes de rendu FXG intégrées {#section-c817e4b4f7da414ea5a51252ca7e120a}

Lorsque le moteur de rendu graphique FXG (ou [!DNL AGMServer]) est installé et activé avec la diffusion d’images, les requêtes FXG peuvent être utilisées comme sources de calques en les spécifiant dans des commandes `src=` (ou `mask=`). Utilisez la syntaxe suivante :

`…&src=fxg( renderRequest)&…`

Le jeton `fxg` respecte la casse.

>[!NOTE]
>
>Le rendu des graphiques FXG est disponible uniquement dans l’environnement hébergé de Dynamic Media et peut nécessiter une licence supplémentaire. Pour plus d’informations, contactez le support technique de Dynamic Media.

*[!DNL renderRequest]* est la requête de rendu FXG habituelle, à l’exclusion du chemin d’accès racine HTTP ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Les caractères de délimiteur ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes FXG suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Sources d’images étrangères {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Le service d’images prend en charge l’accès aux images sources sur les serveurs HTTP étrangers.

>[!NOTE]
>
>Seul le protocole HTTP est pris en charge pour les URL distantes.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=`, délimitez l’URL étrangère ou le fragment d’URL par des parenthèses :

`…&src=( foreignUrl)&…`

Important Les caractères de délimitation ( `'(',')'`) et les caractères de délimitation de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives aux `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et l’attribut : `AllowDirectUrls` est 0, ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Bien que les URL étrangères ne puissent pas être spécifiées directement dans le composant de chemin de l’URL de requête, il est possible de configurer une règle de prétraitement pour permettre la conversion de chemins d’accès relatifs en URL absolues (voir l’exemple ci-dessous).

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus avec la réponse HTTP. Si aucun en-tête de réponse HTTP `ETag` ou Last-Modified n’est présent, la réponse n’est pas mise en cache. Cela peut entraîner de mauvaises performances pour les accès répétés à la même image étrangère, car la diffusion d’images doit récupérer à nouveau et revalider l’image à chaque accès.

Ce mécanisme prend en charge les mêmes formats de fichiers image que ceux pris en charge par l’utilitaire Conversion d’image (IC), à l’exception des images sources avec 16 bits par composant.

>[!NOTE]
>
>La diffusion d’images exécute automatiquement l’utilitaire de validation lorsqu’une image étrangère est utilisée pour la première fois, afin de s’assurer que l’image est valide et n’a pas été corrompue lors de la transmission. Cela peut entraîner un léger retard au premier accès. Pour de meilleures performances, il est recommandé de limiter la taille de ces images et/ou d’utiliser un format de fichier image qui se compresse correctement.

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

La taille de l’image générée par des requêtes imbriquées/intégrées est normalement optimisée automatiquement. Si la mise en cache des images de requête imbriquées est activée, des gains de performances incrémentiels peuvent être obtenus en spécifiant la taille exacte de l’image imbriquée, de sorte qu’aucune mise à l’échelle supplémentaire ne soit nécessaire lorsque l’entrée de cache est réutilisée.

La diffusion d’images importante ne prend pas en charge le double codage des requêtes imbriquées ou incorporées. Les requêtes imbriquées et incorporées doivent être codées en HTTP comme les requêtes simples.

## Exemples {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modèle de calque avec mise en cache :**

Utilisez l’imbrication pour ajouter la mise en cache à un modèle de calque. Un nombre limité d’images d’arrière-plan sont recouvertes de texte très variable. La chaîne de modèle initiale peut se présenter comme suit :

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Avec de légères modifications, nous pouvons pré-dimensionner l’image de la couche 0 et la mettre en cache de manière persistante, réduisant ainsi la charge du serveur :

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporation de requêtes pour le rendu d’images Dynamic Media**

À l’aide d’un modèle stocké dans [!DNL myCatalog/myTemplate] ; générez l’image pour la couche 2 du modèle à l’aide du rendu d’image Dynamic Media :

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Notez les accolades imbriquées. La requête de rendu d’image incorpore un appel au service d’images pour récupérer une texture répétable.

## Voir aussi {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Référence de rendu d’image, [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Utilitaires de diffusion d’images](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
