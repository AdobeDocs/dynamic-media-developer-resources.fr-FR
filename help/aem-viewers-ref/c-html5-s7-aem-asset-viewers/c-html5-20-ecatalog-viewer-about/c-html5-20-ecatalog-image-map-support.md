---
description: La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus du  principal du.
seo-description: La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus du  principal du.
seo-title: Prise en charge des zones cliquables
solution: Experience Manager
title: Prise en charge des zones cliquables
topic: Dynamic media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge des zones cliquables{#image-map-support}

La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus du  principal du.

L’aspect des icônes de zone cliquable est contrôlé via CSS, comme décrit dans la section Effet [](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)Zone cliquable.

Les zones cliquables exécutent l’une des trois actions suivantes : redirigez vers une page Web externe, le panneau Infos  des  contextuels et des hyperliens internes.

## Redirection vers une page Web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’ `href` attribut de la zone cliquable comporte une URL vers la ressource externe, soit spécifiée explicitement, soit encapsulée dans l’une des fonctions de modèle JavaScript prises en charge : `loadProduct()`, `loadProductCW()`et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la `loadProduct()` fonction :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. Par conséquent, assurez-vous que le code JavaScript est sécurisé.

## Fenêtre contextuelle du panneau d’informations  {#section-7aa036420af646d1ad8cdc388add0b57}

Pour travailler avec les panneaux d’informations, une zone cliquable a l’ `ROLLOVER_KEY` attribut défini. Définissez également l’ `href` attribut en même temps, sinon le traitement de l’URL externe interfère avec le contextuel  panneau Infos.

Enfin, assurez-vous que la configuration du lecteur de contenu inclut les valeurs appropriées pour `InfoPanelPopup.template` et, éventuellement, `InfoPanelPopup.infoServerUrl` les paramètres.

>[!NOTE]
>
>Sachez que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et ce code JavaScript sont sécurisés.

## Hyperliens internes {#section-6afa4fb2fe564c429e0201f019a95849}

Le fait de cliquer sur une zone cliquable permet d’effectuer une permutation de page interne dans la visionneuse. Pour utiliser cette fonctionnalité, un attribut de la zone cliquable `href` possède le format spécial suivant :

` href=target: *`idx`*`

où ` *`idx`*` est un index de base zéro de la planche de catalogue.

Vous trouverez ci-dessous un exemple d’ `href` attribut pour une zone cliquable qui pointe vers la planche 3D dans le catalogue électronique :

`href=target:2`
