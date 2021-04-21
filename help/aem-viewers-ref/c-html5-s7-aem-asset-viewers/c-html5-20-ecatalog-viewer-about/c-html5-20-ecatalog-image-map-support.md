---
description: La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.
solution: Experience Manager
title: Prise en charge des zones cliquables
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Prise en charge des zones cliquables{#image-map-support}

La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.

L’aspect des icônes de mappage est contrôlé via CSS, comme décrit dans [Effet de zone cliquable](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Les zones cliquables effectuent l’une des trois actions suivantes : redirection vers une page Web externe, une activation contextuelle du panneau Infos et des hyperliens internes.

## Redirection vers une page Web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attribut `href` de la zone cliquable comporte une URL vers la ressource externe, soit explicitement spécifiée, soit encapsulée dans l’une des fonctions de modèle JavaScript prises en charge : `loadProduct()`, `loadProductCW()` et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la fonction `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Notez que lorsque vous ajoutez le code JavaScript dans l’attribut `HREF` de votre zone cliquable, le code est exécuté sur l’ordinateur du client. Par conséquent, assurez-vous que le code JavaScript est sécurisé.

## Activation contextuelle du panneau d’informations {#section-7aa036420af646d1ad8cdc388add0b57}

Pour utiliser les panneaux d’informations, une zone cliquable a l’attribut `ROLLOVER_KEY` défini. En outre, définissez l’attribut `href` en même temps, sinon le traitement des URL externes interfère avec l’activation contextuelle du panneau Infos.

Enfin, veillez à ce que la configuration de la visionneuse comprenne les valeurs appropriées pour les paramètres `InfoPanelPopup.template` et, éventuellement, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Notez que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et ce code JavaScript sont sécurisés.

## Hyperliens internes {#section-6afa4fb2fe564c429e0201f019a95849}

Le fait de cliquer sur une zone cliquable permet d’effectuer une permutation de page interne dans la visionneuse. Pour utiliser cette fonctionnalité, un attribut `href` dans la zone cliquable présente le format spécial suivant :

` href=target: *`idx`*`

où `*`idx`*` est un index de base zéro de l&#39;étendue du catalogue.

Vous trouverez ci-dessous un exemple d’attribut `href` pour une zone cliquable pointant vers l’étendue 3D du catalogue électronique :

`href=target:2`
