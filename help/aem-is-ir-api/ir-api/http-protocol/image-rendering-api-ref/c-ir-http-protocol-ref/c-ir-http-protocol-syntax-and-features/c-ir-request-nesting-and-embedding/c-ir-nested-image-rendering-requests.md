---
title: Demandes de rendu d’image imbriquées
description: Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir du service d’images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Demandes de rendu d’image imbriquées{#nested-image-rendering-requests}

Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image matérielle, tout comme une image obtenue à partir du service d’images.

Une demande de rendu peut être utilisée comme image matérielle en la spécifiant dans la variable `src=` comme suit :

` …&src=ir{ *[!DNL renderRequest]*}&…`

Le `ir` est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin racine de rendu d’image (généralement `http:// *[!DNL server]*/ir/render/'`), mais peut inclure des jetons de règle de prétraitement.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de la requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Également ignorés `attribute::MaxPix` et `attribute::DefaultPix` du catalogue de matières qui s’applique à la demande de rendu imbriquée.

Le résultat de l’image d’une requête IR imbriquée peut être mis en cache de manière facultative en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire est réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
