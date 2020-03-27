---
description: Une demande Image Server (IS) peut être utilisée comme image matérielle.
seo-description: Une demande Image Server (IS) peut être utilisée comme image matérielle.
seo-title: Requêtes Image Server intégrées
solution: Experience Manager
title: Requêtes Image Server intégrées
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Requêtes Image Server intégrées{#embedded-image-server-requests}

Une demande Image Server (IS) peut être utilisée comme image matérielle.

Spécifiez la requête dans la `src=` commande comme suit :

` …&src=is( *[!DNL imageServingRequest]*)&…`

Le `is` jeton est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin racine du serveur d’images (généralement [!DNL http:// *[!DNL server]*/is/image/&quot;]), mais peut inclure des jetons de règle de prétraitement.

Les commandes IS suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de la requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Sont également ignorés `attribute::MaxPix` et le catalogue `attribute::DefaultPix` d’images qui s’applique à la demande IS incorporée.

Si l’image de résultat de la requête imbriquée inclut des données de masque (alpha), elle est toujours transmise au matériau. Utilisez un calque d’image d’arrière-plan en couleur unie pour éviter les effets alpha indésirables.

Le résultat de l’image d’une demande IS incorporée peut être mis en cache, éventuellement, en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
