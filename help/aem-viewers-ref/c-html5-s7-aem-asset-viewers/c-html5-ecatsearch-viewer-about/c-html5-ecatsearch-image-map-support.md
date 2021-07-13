---
description: La visionneuse de recherche de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.
solution: Experience Manager
title: Prise en charge des zones cliquables
feature: Dynamic Media Classic,Visionneuses,SDK/API,Recherche catalogue électronique
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Prise en charge des zones cliquables{#image-map-support}

La visionneuse de recherche de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.

L’aspect des icônes de carte est contrôlé via CSS, comme décrit dans [Effet de zone cliquable](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Les zones cliquables effectuent l’une des trois actions suivantes : rediriger vers une page web externe, l’activation contextuelle du panneau Informations et les liens hypertextes internes.

## Redirection vers une page web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attribut `href` de la zone cliquable comporte une URL vers la ressource externe, soit spécifiée explicitement, soit encapsulée dans l’une des fonctions de modèle JavaScript prises en charge : `loadProduct()`, `loadProductCW()` et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la fonction `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

N’oubliez pas que lorsque vous ajoutez le code JavaScript dans l’attribut `HREF` de votre zone cliquable, celui-ci est exécuté sur l’ordinateur du client. Par conséquent, assurez-vous que le code JavaScript est sécurisé.

## Activation de la fenêtre contextuelle du panneau d’informations {#section-7aa036420af646d1ad8cdc388add0b57}

Pour utiliser les panneaux Informations, une zone cliquable est associée à l’attribut `ROLLOVER_KEY` . Définissez également l’attribut `href` en même temps, sinon le traitement des URL externes interfère avec l’activation contextuelle du panneau Informations.

Enfin, assurez-vous que la configuration de la visionneuse inclut les valeurs appropriées pour les paramètres `InfoPanelPopup.template` et, éventuellement, les paramètres `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Gardez à l’esprit que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et ce code JavaScript sont sécurisés.

## Liens hypertextes internes {#section-6afa4fb2fe564c429e0201f019a95849}

Cliquer sur une zone cliquable permet d’effectuer un échange de page interne dans la visionneuse. Pour utiliser cette fonctionnalité, un attribut `href` de la zone cliquable a le format spécial suivant :

` href=target: *`idx`*`

où `*`idx`*` est un index de base zéro de la propagation du catalogue.

Voici un exemple d’attribut `href` pour une zone cliquable qui pointe vers la diffusion 3D dans le catalogue électronique :

`href=target:2`
