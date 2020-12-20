---
description: Mode de rendu de conversion des couleurs. Fournit le mode de rendu par défaut pour les conversions de couleur lorsque le mode de rendu n’est pas spécifié avec icc=.
seo-description: Mode de rendu de conversion des couleurs. Fournit le mode de rendu par défaut pour les conversions de couleur lorsque le mode de rendu n’est pas spécifié avec icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Scene7 Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

Mode de rendu de conversion des couleurs. Fournit le mode de rendu par défaut pour les conversions de couleur lorsque le mode de rendu n’est pas spécifié avec icc=.

## Propriétés {#section-0a38c60e1525426185616c42824aee2c}

Enum. Définissez cette valeur sur 0 pour la perception, 1 pour la colorimétrique relative, 2 pour la saturation, 3 pour la colorimétrique absolue. N’indiquez rien ou définissez une autre valeur pour utiliser le mode de rendu par défaut défini dans le profil de couleurs.

## Par défaut {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Hérité de `default::IccRenderIntent`si elle n&#39;est pas définie. Si la valeur est vide, l’option &quot;colorimétrique relatif&quot; est appliquée.

## Voir aussi {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribut ::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [attribut ::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
