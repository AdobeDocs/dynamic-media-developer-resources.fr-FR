---
description: Une demande Image Server (IS) peut être utilisée comme image matérielle.
seo-description: Une demande Image Server (IS) peut être utilisée comme image matérielle.
seo-title: Requêtes Image Server incorporées
solution: Experience Manager
title: Requêtes Image Server incorporées
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Requêtes Image Server incorporées{#embedded-image-server-requests}

Une demande Image Server (IS) peut être utilisée comme image matérielle.

Spécifiez la requête dans la commande `src=` comme suit :

` …&src=is( *[!DNL imageServingRequest]*)&…`

Le jeton `is` est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin racine de diffusion d’images (généralement [ ! DNL http:// *[!DNL server]*/is/image/&quot;]), mais peut inclure des jetons de règle de prétraitement.

Les commandes IS suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (soit dans l’URL de la requête, soit dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

`attribute::MaxPix` et `attribute::DefaultPix` du catalogue d’images qui s’applique à la demande IS incorporée sont également ignorés.

Si l’image de résultat de la requête imbriquée inclut des données de masque (alpha), elle est toujours transmise à la matière. Utilisez un calque d’image d’arrière-plan de couleur unie pour éviter les couches alpha indésirables.

Le résultat d&#39;image d&#39;une demande IS incorporée peut être mis en cache éventuellement en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre demande dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
