---
description: Données de cible de zoom. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de visionneuse de zoom.
solution: Experience Manager
title: Cibles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Cibles{#targets}

Données de cible de zoom. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de visionneuse de zoom.

Le serveur renvoie le contenu de ce champ en réponse à `req=targets`, après avoir remplacé les jetons &#39; &#39; terminator d’enregistrement `??`.

Vous pouvez associer jusqu’à quatre propriétés à chaque cible de zoom :

` Target. *` `*.frame= *`image numérique`*`

` Target. *` `*.rect= *`num gauche, haut, largeur, hauteur`*`

` Target. *` `*.label= *`libellé numérique`*`

` Target. *` `*.userData= *`num userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Num </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de cibles de zoom (int) ; Les cibles de zoom doivent être numérotées de façon séquentielle et consécutive, en commençant par 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> cadre </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro de cadre/page facultatif pour cibler un cadre/une page spécifique d’une visionneuse à 360° ou d’un ensemble de brochures ; la valeur par défaut est 0 si elle n’est pas spécifiée pour l’utilisation de la visionneuse à 360° et de la visionneuse de brochure ; ignoré par la visionneuse de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> gauche, haut </span> </span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels entre le coin supérieur gauche de l’image et le coin supérieur gauche du rectangle de la cible de zoom (int, int) ; doit être égale ou supérieure à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> width, height </span> </span> </p> </td> 
  <td class="stentry"> <p>Taille en pixels du rectangle cible de zoom (int, int) ; doit être supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> étiquette </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de données textuelles ; peut être utilisée comme libellé de texte pour un lien de cibles de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Données </span> utilisateur </span> </p> </td> 
  <td class="stentry"> <p>Valeur de données textuelles ; peut être utilisé pour transmettre des informations spécifiques à la cible au client, telles qu’une valeur SKU ou une URL de lien dynamique. </p> </td> 
 </tr> 
</table>

Cible. *`num`*.rect est requis pour chaque cible de zoom et doit spécifier un rectangle entièrement dans l’image. Toutes les autres propriétés sont facultatives.

*`label`* et *`userData`* participer à la localisation de chaînes de textes. Pour plus d’informations, reportez-vous à [la section Localisation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) de chaînes de texte dans la section Référence *du* protocole HTTP.

Pour les applications impliquant les clients de visionneuse de spin et de brochure, les cibles de zoom doivent être définies dans le même enregistrement de catalogue qui définit la visionneuse d’images. Toutes les définitions de cibles de zoom dans les enregistrements de catalogue des membres de la visionneuse d’images sont ignorées par le visualiseur.

Les Dynamic Media spectateurs attendent des cibles de zoom dans les coordonnées de l’image pleine résolution déjà ajustées par les commandes de `catalog::Modifier`.

## Propriétés {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valeur des données de](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) propriété.

## Par défaut {#section-feab29f6575e482391086a57f547543c}

Aucune

## Voir aussi {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog ::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog ::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localisation d’une chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
