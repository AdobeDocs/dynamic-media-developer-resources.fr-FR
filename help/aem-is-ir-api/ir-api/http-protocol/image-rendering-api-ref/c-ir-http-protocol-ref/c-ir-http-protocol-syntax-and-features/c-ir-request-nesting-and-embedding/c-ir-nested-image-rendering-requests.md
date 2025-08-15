---
title: Demandes de rendu d’images imbriquées
description: Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir d’Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Demandes de rendu d’images imbriquées{#nested-image-rendering-requests}

Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir d’Image Server.

Une demande de rendu peut être utilisée comme image de matériau en la spécifiant dans la `src=` commande comme suit :

` …&src=ir{ *[!DNL renderRequest]*}&…`

Le `ir` jeton est sensible à la casse.

La demande imbriquée ne doit pas inclure le chemin racine Image Rendering (généralement `http:// *[!DNL server]*/ir/render/'`), mais peut inclure des jetons de règle de prétraitement.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (soit dans l’URL de la requête, soit dans ou dans `catalog::Modifier` `catalog::PostModifier`:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Sont `attribute::MaxPix` également ignorés et `attribute::DefaultPix` du catalogue de matériaux qui s’applique à la demande de rendu imbriquée.

Le résultat d’image d’une demande IR imbriquée peut éventuellement être mis en cache en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire est réutilisée dans une autre demande dans un délai raisonnable. La gestion standard de la mémoire cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
