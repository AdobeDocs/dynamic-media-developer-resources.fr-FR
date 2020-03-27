---
description: Le rendu d’image prend en charge les conversions d’espace colorimétrique en fonction des d’espace colorimétrique  conformes à la spécification ICC (International Color Consortium).
seo-description: Le rendu d’image prend en charge les conversions d’espace colorimétrique en fonction des d’espace colorimétrique  conformes à la spécification ICC (International Color Consortium).
seo-title: Gestion des couleurs de rendu d’image *
solution: Experience Manager
title: Gestion des couleurs de rendu d’image *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Gestion des couleurs de rendu d’image *{#image-rendering-color-management}

Le rendu d’image prend en charge les conversions d’espace colorimétrique en fonction des d’espace colorimétrique  conformes à la spécification ICC (International Color Consortium).

**Restrictions**

Seuls les espaces colorimétriques CMJN, RVB et Niveaux de gris sont actuellement pris en charge.

Les fichiers de style d’armoire (.vnc) et les fichiers de style de garniture de fenêtre ( [!DNL .vnw]) ne sont pas gérés par les couleurs et sont supposés exister dans l’espace colorimétrique de travail.

**Voir aussi**

[International Color Consortium](http://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ , `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`,  ,  ,  ,  , ICC`attribute::IccRenderIntent``attribute::IccBlackPointCompensation``attribute::IccDither`

## Espaces colorimétriques par défaut {#section-8ce27edf42e746febe4654f8f19b9c0c}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de  ICC. Ces  constituent les espaces colorimétriques par défaut de ce catalogue : une entrée et un de sortie  chacun pour les données en niveaux de gris, RVB et CMJN ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`et `attribute::IccProfileSrcCmyk`).

L’espace colorimétrique par défaut d’une image ou d’un autre objet est sélectionné dans le par défaut du catalogue en fonction du type de pixel de l’image.

## Espace colorimétrique d’entrée {#section-660f661a7e954df4b451e34134195276}

Les images de matériau peuvent incorporer des  ICC pour définir l’espace colorimétrique d’entrée. Si aucun  de n’est incorporé dans une image source, le catalogue `attribute::IccProfileSrc*` d’images correspondant au type de pixel de l’image source est utilisé. Si cet attribut n’est pas défini dans le catalogue d’images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par les couleurs et seules les transformations naïves sont appliquées.

## Espace colorimétrique de travail {#section-645d9cfa5b0347a190a0ece218f5b5e1}

En règle générale, l’espace colorimétrique de travail est défini par le de couleurs ICC  intégré dans la vignette. Si la vignette n’inclut pas de , le d’entrée RVB par défaut ( `attribute::IccProfileSrcRgb` du catalogue de session) est utilisé pour l’espace colorimétrique de travail.

Toutes les opérations de rendu sont exécutées dans l’espace colorimétrique de travail.

**Important :** Le ICC de l’espace colorimétrique de travail doit prendre en charge les transformations d’entrée et de sortie. Si un en sortie uniquement est utilisé comme IR de l’espace colorimétrique de travail, il ne sera pas possible de convertir les matériaux en cet espace colorimétrique de travail. Un tel de couleurs peut encore être utilisé si des matériaux existent dans le même espace colorimétrique de travail. Toute tentative d&#39;application de matériaux dans d&#39;autres espaces colorimétriques échouera.

## Valeurs de couleur explicites {#section-31727bf1b23e477ca92572fbbf422d2f}

Les valeurs de couleur RVB spécifiées avec `color=`, `bgc=`, `catalog::BgColor`et `catalog::Color` sont supposées exister dans l’espace colorimétrique de travail actuel.

## Fichiers de données matières {#section-33f7a170a6664c02b8479fb89cc0aea3}

Les fichiers d’image de matériau (images de texture et de décal) peuvent être de type RVB, Niveaux de gris ou CMJN et peuvent incorporer un  de couleurs. Si aucun de couleurs n’est incorporé, l’espace colorimétrique d’entrée par défaut est associé à l’image (par exemple, le de couleurs  du catalogue de matériaux qui correspond au type de pixel de l’image).

Les images matérielles obtenues à partir des demandes imbriquées de diffusion d’images ou de rendu d’images incluent généralement un  de couleur. Dans le cas contraire, les images sont associées à l’espace colorimétrique d’entrée par défaut correspondant au type de pixel.

Si l’espace colorimétrique du fichier image est différent de celui de l’espace colorimétrique de travail, une conversion des couleurs précise est utilisée pour la conversion dans l’espace colorimétrique de travail. La conversion de type naïf est utilisée lorsqu’aucun  de n’est incorporé et qu’aucun d’entrée par défaut n’est défini.

D’autres fichiers de données, tels que les fichiers de style d’armoire ( [!DNL .vnc]) ou les fichiers de garniture de fenêtre ( [!DNL .vnw]), n’intègrent pas les  de couleurs et sont toujours considérés comme faisant partie de l’espace colorimétrique de travail.

## Espace colorimétrique de sortie {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Toutes les opérations de rendu ont lieu dans l’espace colorimétrique de travail. Si la requête spécifie un de couleurs différent avec la `icc=` commande, les données sont converties dans cet espace colorimétrique juste avant d’être codées et renvoyées au client. Lorsque la gestion des couleurs est désactivée, la conversion naïve est utilisée si nécessaire pour la conversion en niveaux de gris ou en CMJN.

## de couleurs intégré {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Le de couleurs associé à l’image rendue peut être incorporé dans l’image de réponse en spécifiant `iccEmbed=` la requête.

Si `icc=` ce n’est pas le cas, le  ICC de l’espace colorimétrique de travail est incorporé. Aucune  de n’est incorporée si la gestion des couleurs est désactivée et qu’aucun  de n’a été spécifié avec `icc=`.

## Profils ICC {#section-afeb76068b5042adb83261638e450140}

Tous les de couleurs utilisés par le serveur doivent être conformes aux spécifications ICC. Les fichiers  ICC ont généralement un suffixe [!DNL .icc] ou [!DNL .icm] un suffixe de fichier et sont colocalisés avec les fichiers de données de matériau.

Bien que les  de sortie puissent être spécifiées par chemin/nom de fichier dans la `icc=` commande, il est recommandé d’enregistrer tous les fichiers  de sortie dans la carte de  ICC du catalogue par défaut ou d’un catalogue de matières spécifique et d’utiliser des identifiants de raccourci ( `icc::Name`) au lieu des chemins d’accès aux fichiers.

Le de travail doit être enregistré dans la carte de ICC du catalogue de matières ou du catalogue par défaut.
