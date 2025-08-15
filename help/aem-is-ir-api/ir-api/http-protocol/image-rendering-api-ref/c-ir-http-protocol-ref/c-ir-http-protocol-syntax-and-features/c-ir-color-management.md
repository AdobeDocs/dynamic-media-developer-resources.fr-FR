---
description: Le rendu d’image prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).
solution: Experience Manager
title: Gestion des couleurs du rendu des images *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Gestion des couleurs du rendu des images *{#image-rendering-color-management}

Le rendu d’image prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).

**Restrictions**

Seuls les espaces colorimétriques CMJN, RGB et de niveaux de gris sont actuellement pris en charge.

Les fichiers de style d’armoire (.vnc) et de couvre-fenêtres ( [!DNL .vnw]) ne sont pas gérés par les couleurs et sont supposés exister dans l’espace colorimétrique de travail.

**Voir aussi**

[International Color Consortium](https://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , Cartes de profil ICC

## Espaces colorimétriques par défaut {#section-8ce27edf42e746febe4654f8f19b9c0c}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de profils ICC. Ces profils constituent les espaces colorimétriques par défaut de ce catalogue : un profil d’entrée et un profil de sortie chacun pour les données en niveaux de gris, RGB et CMJN ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` et `attribute::IccProfileSrcCmyk`).

L’espace colorimétrique par défaut d’une image particulière ou d’un autre objet est sélectionné dans les profils par défaut du catalogue en fonction du type de pixel de l’image.

## Espace colorimétrique d’entrée {#section-660f661a7e954df4b451e34134195276}

Les images de matériau peuvent incorporer des profils ICC pour définir l’espace colorimétrique d’entrée. Si aucun profil n’est incorporé dans une image source, `attribute::IccProfileSrc*` du catalogue d’images applicable correspondant au type de pixel de l’image source est utilisé. Si cet attribut n’est pas défini dans le catalogue d’images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par couleur et seules les transformations naïves sont appliquées.

## Espace colorimétrique de travail {#section-645d9cfa5b0347a190a0ece218f5b5e1}

En règle générale, l’espace colorimétrique de travail est défini par le profil colorimétrique ICC intégré à la vignette. Si la vignette n’inclut pas de profil, le profil d’entrée RGB par défaut (`attribute::IccProfileSrcRgb` du catalogue de sessions) est utilisé pour l’espace colorimétrique de travail.

Toutes les opérations de rendu sont exécutées dans l’espace colorimétrique de travail.

**Important :** le profil ICC de l’espace colorimétrique de travail doit prendre en charge les transformations d’entrée et de sortie. Si un profil de sortie seule est utilisé comme espace colorimétrique de travail, IR ne peut pas y convertir les matériaux. Un tel profil de couleurs peut encore être utilisé si des matériaux existent dans le même espace colorimétrique de travail. Toute tentative d’application de matériaux dans d’autres espaces colorimétriques échoue.

## Valeurs de couleur explicites {#section-31727bf1b23e477ca92572fbbf422d2f}

Les valeurs de couleur RGB spécifiées avec `color=`, `bgc=`, `catalog::BgColor` et `catalog::Color` sont supposées exister dans l’espace colorimétrique de travail actuel.

## Fichiers de données des matériaux {#section-33f7a170a6664c02b8479fb89cc0aea3}

Les fichiers d’image de matériau (images de texture et de décalcomanie) peuvent être de type RGB, niveaux de gris ou pixels CMJN et peuvent incorporer un profil de couleurs. Si aucun profil colorimétrique n’est incorporé, l’espace colorimétrique d’entrée par défaut est associé à l’image (par exemple, le profil colorimétrique du catalogue des matériaux, qui correspond au type de pixel de l’image).

Les images de matériau obtenues à partir de requêtes de diffusion d’images imbriquées ou de rendu d’image incluent généralement un profil de couleurs. Si ce n’est pas le cas, les images sont associées à l’espace colorimétrique d’entrée par défaut correspondant au type de pixel.

Si l’espace colorimétrique du fichier image est différent de l’espace colorimétrique de travail, une conversion de couleurs précise est utilisée pour effectuer la conversion dans l’espace colorimétrique de travail. La conversion de type naïf est utilisée lorsqu’aucun profil n’est incorporé et qu’aucun profil d’entrée par défaut n’est défini.

D’autres fichiers de données de matériaux, tels que les fichiers de style armoire ([!DNL .vnc]) ou les fichiers de recouvrement de fenêtre ([!DNL .vnw]), n’intègrent pas les profils de couleurs et sont toujours supposés se trouver dans l’espace colorimétrique de travail.

## Espace colorimétrique de sortie {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Toutes les opérations de rendu ont lieu dans l’espace colorimétrique de travail. Si la requête spécifie un profil colorimétrique différent avec la commande `icc=`, les données sont converties dans cet espace colorimétrique juste avant d’être codées et renvoyées au client. Lorsque la gestion des couleurs est désactivée, une conversion naïve est utilisée si nécessaire pour effectuer une conversion en niveaux de gris ou en CMJN.

## Profils de couleurs incorporés {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Le profil de couleurs associé à l’image rendue peut être incorporé dans l’image de réponse en spécifiant `iccEmbed=` pour la requête.

Si `icc=` n’est pas spécifié, le profil ICC de l’espace colorimétrique de travail est incorporé. Aucun profil n’est incorporé si la gestion des couleurs est désactivée et qu’aucun profil n’a été spécifié avec `icc=`.

## Profils ICC {#section-afeb76068b5042adb83261638e450140}

Tous les profils de couleurs utilisés par le serveur doivent être conformes à la spécification ICC. Les fichiers de profil ICC ont généralement un suffixe de fichier [!DNL .icc] ou [!DNL .icm] et sont co-localisés avec les fichiers de données de matériaux.

Bien que les profils de sortie puissent être spécifiés par chemin/nom de fichier dans la commande `icc=`, il est recommandé d&#39;enregistrer tous les fichiers de profil dans la carte de profil ICC du catalogue par défaut ou d&#39;un catalogue de matériaux spécifique et d&#39;utiliser des identifiants de raccourci ( `icc::Name`) au lieu des chemins de fichier.

Les profils de travail doivent être enregistrés dans la carte de profil ICC du catalogue de matériaux ou du catalogue par défaut.
