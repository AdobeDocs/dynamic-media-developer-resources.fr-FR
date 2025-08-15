---
title: Requêtes du serveur d’images intégré
description: Une requête du serveur d’images (IS) peut être utilisée comme image matérielle.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Requêtes du serveur d’images intégré{#embedded-image-server-requests}

Une requête du serveur d’images (IS) peut être utilisée comme image matérielle.

Spécifiez la requête dans la commande `src=` comme suit :

` …&src=is( *[!DNL imageServingRequest]*)&…`

Le jeton `is` respecte la casse.

La requête imbriquée ne doit pas inclure le chemin racine du service d’images (généralement [!DNL http:// *[!DNL server]*/is/image/"]), mais peut inclure des jetons de règle de prétraitement.

Les commandes IS suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de la requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Les `attribute::MaxPix` et `attribute::DefaultPix` du catalogue d’images qui s’appliquent à la requête IS incorporée sont également ignorés.

Si l’image de résultat de la requête imbriquée inclut des données de masque (alpha), elle est toujours transmise au matériau. Utilisez un calque d’image d’arrière-plan en couleur unie pour éviter les caractères alpha indésirables.

Le résultat de l’image d’une requête IS incorporée peut être mis en cache en incluant éventuellement `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire est réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
