---
description: Le rendu d’image prend en charge les conversions d’espace colorimétrique en fonction de profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).
solution: Experience Manager
title: Gestion des couleurs de rendu d’image *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---


# Gestion des couleurs de rendu d’image *{#image-rendering-color-management}

Le rendu d’image prend en charge les conversions d’espace colorimétrique en fonction de profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).

**Restrictions**

Pour le moment, seuls les espaces colorimétriques CMJN, RVB et Niveaux de gris sont pris en charge.

Les fichiers de style d’armoire (.vnc) et les fichiers de style de garnitures de fenêtre ( [!DNL .vnw]) ne sont pas gérés par les couleurs et sont supposés exister dans l’espace colorimétrique de travail.

**Voir aussi**

[International Color Consortium](http://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation` , , ICC Profils Maps`attribute::IccDither`

## Espaces de couleur par défaut {#section-8ce27edf42e746febe4654f8f19b9c0c}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de profils ICC. Ces profils constituent les espaces colorimétriques par défaut de ce catalogue : une entrée et un profil de sortie chacun pour les données en niveaux de gris, RVB et CMJN ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` et `attribute::IccProfileSrcCmyk`).

L’espace colorimétrique par défaut d’une image ou d’un autre objet est sélectionné dans les profils par défaut du catalogue en fonction du type de pixel de l’image.

## Espace colorimétrique d&#39;entrée {#section-660f661a7e954df4b451e34134195276}

Les images de matériau peuvent incorporer des profils ICC pour définir l’espace colorimétrique d’entrée. Si aucun profil n’est incorporé dans une image source, `attribute::IccProfileSrc*` du catalogue d’images approprié correspondant au type de pixel de l’image source est utilisé. Si cet attribut n&#39;est pas défini dans le catalogue d&#39;images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par les couleurs et seules les transformations naïves sont appliquées.

## Espace de couleurs de travail {#section-645d9cfa5b0347a190a0ece218f5b5e1}

En règle générale, l’espace colorimétrique de travail est défini par le profil de couleurs ICC incorporé dans la vignette. Si la vignette n’inclut pas de profil, le profil d’entrée RVB par défaut ( `attribute::IccProfileSrcRgb` du catalogue de sessions) est utilisé pour l’espace colorimétrique de travail.

Toutes les opérations de rendu sont exécutées dans l’espace colorimétrique de travail.

**Important :** Le profil ICC de l’espace colorimétrique de travail doit prendre en charge les transformations d’entrée et de sortie. Si un profil de sortie uniquement est utilisé comme IR d&#39;espace colorimétrique de travail, il ne sera pas possible de convertir des matériaux en ce . Un tel profil colorimétrique peut encore être utilisé si des matériaux existent dans le même espace colorimétrique de travail. La tentative d&#39;application de matériaux dans d&#39;autres espaces colorimétriques échouera.

## Valeurs de couleur explicites {#section-31727bf1b23e477ca92572fbbf422d2f}

Les valeurs de couleur RVB spécifiées avec `color=`, `bgc=`, `catalog::BgColor` et `catalog::Color` sont supposées exister dans l’espace colorimétrique de travail actuel.

## Fichiers de données de matériau {#section-33f7a170a6664c02b8479fb89cc0aea3}

Les fichiers d’image de matériau (images de texture et de décal) peuvent être de type RVB, Niveaux de gris ou CMJN et peuvent incorporer un profil de couleur. Si aucun profil de couleur n’est incorporé, l’espace colorimétrique d’entrée par défaut est associé à l’image (par exemple, le profil de couleur du catalogue de matériaux correspondant au type de pixel de l’image).

Les images matérielles obtenues à partir des demandes de diffusion d’images ou de rendu d’images imbriquées incluent généralement un profil de couleurs. Dans le cas contraire, les images sont associées à l’espace colorimétrique d’entrée par défaut correspondant au type de pixel.

Si l’espace colorimétrique du fichier image est différent de l’espace colorimétrique de travail, une conversion colorimétrique précise est utilisée pour la conversion dans l’espace colorimétrique de travail. La conversion de type naïve est utilisée lorsqu’aucun profil n’est incorporé et qu’aucun profil d’entrée par défaut n’est défini.

Les autres fichiers de données de matériau, tels que les fichiers de style d&#39;armoire ( [!DNL .vnc]) ou les fichiers de recouvrement de fenêtre ( [!DNL .vnw]), n&#39;incorporent pas de profils de couleur et sont toujours supposés se trouver dans l&#39;espace colorimétrique de travail.

## Espace colorimétrique de sortie {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Toutes les opérations de rendu ont lieu dans l’espace colorimétrique de travail. Si la requête spécifie un autre profil de couleurs avec la commande `icc=`, les données seront converties dans cet espace de couleurs juste avant d’être codées et renvoyées au client. Lorsque la gestion des couleurs est désactivée, la conversion naïve est utilisée si nécessaire pour la conversion en niveaux de gris ou en CMJN.

## Profils de couleur incorporés {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Le profil de couleur associé à l’image rendue peut être incorporé à l’image de réponse en spécifiant `iccEmbed=` pour la requête.

Si `icc=` n’est pas spécifié, le profil ICC de l’espace colorimétrique de travail est incorporé. Aucun profil n’est incorporé si la gestion des couleurs est désactivée et aucun profil n’a été spécifié avec `icc=`.

## Profils ICC {#section-afeb76068b5042adb83261638e450140}

Tous les profils de couleur utilisés par le serveur doivent être conformes à la spécification ICC. Les fichiers de profil ICC ont généralement un suffixe de fichier [!DNL .icc] ou [!DNL .icm] et sont colocalisés avec des fichiers de données de matériau.

Bien que les profils de sortie puissent être spécifiés par chemin/nom de fichier dans la commande `icc=`, il est recommandé d&#39;enregistrer tous les fichiers de profil dans la carte de Profil ICC du catalogue par défaut ou d&#39;un catalogue de matières spécifique et d&#39;utiliser des identificateurs de raccourci ( `icc::Name`) au lieu des chemins d&#39;accès aux fichiers.

Les profils de travail doivent être enregistrés dans la carte de Profil ICC du catalogue de matières ou du catalogue par défaut.
