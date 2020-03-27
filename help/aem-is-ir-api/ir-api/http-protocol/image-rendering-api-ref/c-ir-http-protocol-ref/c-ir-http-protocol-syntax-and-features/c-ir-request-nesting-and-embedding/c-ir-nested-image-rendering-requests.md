---
description: Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir de la diffusion d’images.
seo-description: Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir de la diffusion d’images.
seo-title: Demandes de rendu d’image imbriquées
solution: Experience Manager
title: Demandes de rendu d’image imbriquées
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Demandes de rendu d’image imbriquées{#nested-image-rendering-requests}

Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir de la diffusion d’images.

Une demande de rendu peut être utilisée comme image matérielle en la spécifiant dans la `src=` commande comme suit :

` …&src=ir{ *[!DNL renderRequest]*}&…`

Le `ir` jeton est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin racine de rendu d’image (généralement `http:// *[!DNL server]*/ir/render/'`), mais peut inclure des jetons de règle de prétraitement.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Sont également ignorés `attribute::MaxPix` et le catalogue `attribute::DefaultPix` de matières qui s’applique à la demande de rendu imbriquée.

Le résultat de l’image d’une requête IR imbriquée peut être mis en cache en option en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
