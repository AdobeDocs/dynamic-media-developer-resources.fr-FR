---
title: defaultImage
description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
TQID: 'https://experienceleague.adobe.com/48NrVSWIy5golPIibmMEc9FeoE24MtwxfEiYV35k7k4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 1%

---

# defaultImage{#defaultimage}

Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.

` defaultImage= *`objet`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objet <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>Objet image. </p> </td> 
 </tr> 
</table>

*`object`* peut être une entrée de catalogue (y compris un modèle) ou un simple chemin d’accès au fichier image. Utile pour remplacer des images manquantes par des images par défaut. Cette valeur remplace la valeur de la `attribute::DefaultImage` de catalogue correspondante. Une valeur vide ( `defaultImage=`) désactive la gestion des images par défaut.

>[!NOTE]
>
>Le mécanisme d’image par défaut ne s’applique pas aux objets SVG. Une erreur est renvoyée si l’objet SVG spécifié dans la requête est introuvable.

Si `attribute::DefaultImageMode=0`, *`object`* remplace l’intégralité de la requête d’origine, même si une seule image d’une composition multi-images est manquante. Les seules commandes conservées à partir de la requête d’origine sont les suivantes : `wid=`, `hei=`, `fmt=` et `qlt=`.

Si `attribute::DefaultImageMode=1`, l’objet remplace uniquement l’image du calque manquant ; les attributs du calque manquant sont appliqués, et le composite est traité et renvoyé comme d’habitude.

## Propriétés {#section-d30923d8dc4042eba10989212dd70887}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si `req=` est autre que `img` ou `tmb`.

## Restrictions {#section-30df31bc8cac41cd917f1e45196779c2}

Les sources d’images étrangères ne sont pas couvertes par le mécanisme d’image par défaut. Une erreur est renvoyée si une source d’images étrangères n’est pas valide.

La diffusion d’images revient à la `DefaultImageMode=0` lorsque le rendu d’image imbriqué ou les requêtes de rendu FXG échouent.

## Par défaut {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Voir aussi {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute:: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
