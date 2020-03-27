---
description: Cette section décrit les commandes du protocole HTTP.
seo-description: Cette section décrit les commandes du protocole HTTP.
seo-title: Référence de commande
solution: Experience Manager
title: Référence de commande
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f

---


# Référence de commande{#command-reference}

Cette section décrit les commandes du protocole HTTP.

**Contenu multimédia dynamique dans AEM uniquement**: Outre les paramètres d’image de base disponibles dans l’interface utilisateur, [!DNL Dynamic Media] dans AEM ( [!DNL Adobe Experience Manager]) prend en charge de nombreuses modifications d’image avancées que vous pouvez spécifier dans le champ **Image Modifiers** . Ces paramètres sont définis ci-dessous. Sachez toutefois que les fonctionnalités suivantes ne sont pas prises en charge dans Contenu multimédia dynamique dans AEM.

* Commandes de correction des couleurs : `icc=` et `iccEmbed=`.
* Commandes de base de création de modèles et de rendu de texte : `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` et `textPs=`.
* Commandes de  : `locale=` et `req=xlate`.
* `req=set` n’est pas disponible pour une utilisation générale.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Services de médias dynamiques non principaux : SVG, rendu d’image et impression en ligne.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Reportez-vous également aux Options [de paramètre prédéfini d’](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options) image de média dynamique dans la documentation AEM 6.5.

* [aligner](r-align.md)
* [ancrage](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [Recadrer](r-crop.md)
* [culturePathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [effet](r-effect.md)
* [effectMask](r-effectmask.md)
* [étendre](r-extend.md)
* [ajuster](r-fit.md)
* [flip](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [masquer](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [calque](r-layer.md)
* [locale](r-locale.md)
* [carte](r-map.md)
* [masquer](r-mask.md)
* [maskUse](r-maskuse.md)
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
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [origin](r-origin.md)
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
* [rotate](r-rotate.md)
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
