---
description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.
seo-description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: 46ebb8c7-930e-4844-8664-ec6a63691523
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorDetail{#errordetail}

Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.

Les valeurs suivantes sont autorisées :

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Titre uniquement. Renvoie une brève description générale de l’erreur. Recommandé pour les serveurs en direct accessibles publiquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Bref message. Réservé pour une utilisation ultérieure. Renvoie actuellement les mêmes informations que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Message détaillé. Fournit des détails au niveau de l’utilisateur sur l’erreur. Peut inclure des informations sensibles, telles que les chemins d’accès aux fichiers. Recommandé pour les serveurs d’évaluation, d’assurance qualité et de développement d’applications. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informations complètes sur le débogage. Ajoute des traces de pile Java le cas échéant. Les images d’erreur n’incluent jamais les traces de pile et renvoient les informations de niveau 2 dans <span class="codeph"> $error.message</span>. Ces informations peuvent s’avérer utiles lorsque vous  des problèmes avec l’assistance technique de Scene7. </p></td> 
 </tr> 
</table>

## Propriétés {#section-e167895723ca4ad4ba283d3d7b4324de}

La valeur énumérée doit être 0, 1, 2 ou 3.

## Par défaut {#section-8f27098e509945a18676aca0675c8f41}

Hérité de `default::ErrorDetail` si non spécifié ou si vide.

## Voir aussi {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
