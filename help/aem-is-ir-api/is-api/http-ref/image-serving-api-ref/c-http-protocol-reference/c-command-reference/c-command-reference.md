---
title: Référence de commande
description: Cette section décrit les commandes de protocole HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# Référence de commande{#command-reference}

Cette section décrit les commandes de protocole HTTP.

>[!TIP]
>
>Testez et découvrez les avantages des modificateurs d’image Dynamic Media et de l’imagerie dynamique à l’aide de Dynamic Media [_Snapshot_](https://snapshot.scene7.com/).
>
> L’instantané est un outil de démonstration visuel, conçu pour illustrer la puissance de Dynamic Media pour une diffusion d’images optimisée et dynamique. Testez des images de test ou des URL Dynamic Media afin d’observer visuellement la sortie de divers modificateurs d’image Dynamic Media et d’optimiser l’imagerie dynamique pour les éléments suivants :
>* Taille de fichier (avec diffusion WebP et AVIF)
>* Bande passante réseau
>* RGPD (rapport des pixels de l’appareil)
>
>Pour savoir à quel point il est facile d’utiliser Snapshot, lisez la [vidéo de formation sur les instantanés](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=fr) (3 minutes et 17 secondes).


**Pour Dynamic Media dans Adobe Experience Manager uniquement** - Au-delà des paramètres d’image de base disponibles dans l’interface utilisateur, [!DNL Dynamic Media] dans AEM ( [!DNL Adobe Experience Manager]) prend en charge de nombreuses modifications d’image avancées que vous pouvez spécifier dans le champ **Modificateurs d’image**. Ces paramètres sont définis ci-dessous. Notez toutefois que les fonctionnalités suivantes ne sont pas prises en charge dans Dynamic Media dans AEM.

* Commandes de correction des couleurs : `icc=` et `iccEmbed=`.
* Commandes de base de création de modèles et de rendu de texte : `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` et `textPs=`.
* Commandes de localisation : `locale=` et `req=xlate`.
* `req=set` n’est pas disponible pour une utilisation générale.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Services Dynamic Media non principaux : SVG, rendu d’image et impression en ligne.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Voir également les [Options de paramètre d’image prédéfini](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=fr#dynamic) de Dynamic Media dans la documentation AEM 6.5.

* [align](r-align.md)
* [ancrage](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [couleur](r-color-commandref.md)
* [recadrer](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [effet](r-effect.md)
* [effetMask](r-effectmask.md)
* [étend](r-extend.md)
* [fit](r-fit.md)
* [flip](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [masquer](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [layer](r-layer.md)
* [local](r-locale.md)
* [carte](r-map.md)
* [mask](r-mask.md)
* [maskUse](r-maskuse.md)
* [réseau](r-network.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contraste](r-op-contrast.md)
* [op_grew](r-op-grow.md)
* [op_grewMask](r-op-growmask.md)
* [op_grewMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_bruit](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [origine](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspective](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantifier](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotation](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [taille](r-size-reference.md)
* [src](r-src.md)
* [modèle](r-template.md)
* [texte](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
