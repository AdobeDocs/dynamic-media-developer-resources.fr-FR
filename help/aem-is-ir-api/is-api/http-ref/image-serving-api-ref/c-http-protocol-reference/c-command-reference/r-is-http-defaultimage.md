---
title: defaultImage
description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objet </span> </span> </p> </td> 
  <td class="stentry"> <p>Objet image. </p> </td> 
 </tr> 
</table>

*`object`* peut être une entrée de catalogue (y compris un modèle) ou un simple chemin d’accès au fichier image. Utile pour remplacer les images manquantes par des images par défaut. Cette valeur remplace la valeur du catalogue correspondant `attribute::DefaultImage`. Une valeur vide ( `defaultImage=`) désactive la gestion des images par défaut.

>[!NOTE]
>
>Le mécanisme d’image par défaut ne s’applique pas aux objets SVG. Une erreur est renvoyée si l’objet SVG spécifié dans la requête est introuvable.

Si `attribute::DefaultImageMode=0`, *`object`* remplace l’intégralité de la requête d’origine, même si une seule image dans une composition multi-images est manquante. Les seules commandes conservées à partir de la requête d’origine sont : `wid=`, `hei=`, `fmt=`, `qlt=`.

Si `attribute::DefaultImageMode=1`, l’objet remplace uniquement l’image de couche manquante ; les attributs de la couche manquante sont appliqués et le composite est traité et renvoyé comme d’habitude.

## Propriétés {#section-d30923d8dc4042eba10989212dd70887}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si `req=` est autre que `img` ou `tmb`.

## Restrictions {#section-30df31bc8cac41cd917f1e45196779c2}

Les sources d’images étrangères ne sont pas couvertes par le mécanisme d’image par défaut ; une erreur est renvoyée si une source d’image étrangère n’est pas valide.

La diffusion d’images revient à `DefaultImageMode=0` lorsque les demandes de rendu d’image imbriquées ou FXG échouent.

## Par défaut {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Voir aussi {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
