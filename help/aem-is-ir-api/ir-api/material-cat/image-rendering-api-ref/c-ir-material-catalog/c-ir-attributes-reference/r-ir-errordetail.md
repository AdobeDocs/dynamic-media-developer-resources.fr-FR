---
description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.
seo-description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorDetail{#errordetail}

Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.

## Titre {#section-c10d75d72ee24d16a67cc8d927f1deba}

Les valeurs suivantes sont autorisées :

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Titre uniquement. Renvoie une brève description générale de l’erreur. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Bref message. Réservé pour une utilisation ultérieure. Renvoie actuellement les mêmes informations que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Message détaillé. Fournit des détails au niveau de l’utilisateur sur l’erreur. Peut inclure des informations sensibles, telles que les chemins d’accès aux fichiers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informations complètes sur le débogage. Ajoute des traces de pile Java le cas échéant. Les images d’erreur n’incluent jamais les traces de pile et renvoient les informations de niveau 2 dans <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Le niveau 0 est recommandé pour les serveurs actifs accessibles au public.
* Le niveau 2 est recommandé pour les serveurs d’évaluation, d’assurance qualité et de développement d’applications.
* Les informations de niveau 3 peuvent s’avérer utiles lorsque vous  des problèmes avec l’assistance technique de Scene7.

## Propriétés {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

La valeur énumérée doit être 0, 1, 2 ou 3.

## Par défaut {#section-5e78d550050840cc9a1de811c581b94f}

Hérité de `default::ErrorDetail` si non spécifié ou si vide.

## Voir aussi {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
