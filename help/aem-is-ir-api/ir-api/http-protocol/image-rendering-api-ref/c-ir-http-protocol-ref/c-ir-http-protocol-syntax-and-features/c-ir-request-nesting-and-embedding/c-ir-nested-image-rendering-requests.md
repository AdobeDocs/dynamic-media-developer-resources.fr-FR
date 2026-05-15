---
title: Requêtes de rendu d’image imbriquées
description: Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image de matériau, tout comme une image obtenue à partir de la diffusion d’images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Requêtes de rendu d’image imbriquées{#nested-image-rendering-requests}

Pour les applications avancées, il est possible d’utiliser le résultat d’une opération de rendu comme une image de matériau, tout comme une image obtenue à partir de la diffusion d’images.

Une requête de rendu peut être utilisée comme image de matériau en la spécifiant dans la commande `src=` comme suit :

` …&src=ir{ *[!DNL renderRequest]*}&…`

Le jeton `ir` respecte la casse.

La requête imbriquée ne doit pas inclure le chemin racine de rendu d’image (généralement `http:// *[!DNL server]*/ir/render/'`), mais peut inclure des jetons de règle de prétraitement.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de la requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Les `attribute::MaxPix` et `attribute::DefaultPix` du catalogue de matières qui s’appliquent à la requête de rendu imbriquée sont également ignorés.

Le résultat de l’image d’une requête infrarouge imbriquée peut être mis en cache en incluant éventuellement `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire est réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.
