---
description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 4%

---


# ErrorDetail{#errordetail}

Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.

Les valeurs suivantes sont autorisées :

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Titre uniquement. Renvoie une brève description générale de l’erreur. Recommandé pour les serveurs en direct accessibles au public. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Bref message. Réservé pour une utilisation ultérieure. Renvoie actuellement les mêmes informations que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Message détaillé. Fournit des détails sur l’erreur au niveau de l’utilisateur. Peut inclure des informations sensibles, telles que les chemins d’accès aux fichiers. Recommandé pour les serveurs d’évaluation, d’assurance qualité et de développement d’applications. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informations complètes sur le débogage. Ajoute les traces de la pile Java, le cas échéant. Les images d’erreur n’incluent jamais de traces de pile et renvoient à la place des informations de niveau 2 dans <span class="codeph"> $error.message</span>. Ces informations peuvent s'avérer utiles lorsque des problèmes de rapports se posent au support technique Dynamic Media. </p></td> 
 </tr> 
</table>

## Propriétés {#section-e167895723ca4ad4ba283d3d7b4324de}

Valeur énumérée : 0, 1, 2 ou 3.

## Par défaut {#section-8f27098e509945a18676aca0675c8f41}

Hérité de `default::ErrorDetail` si elle n&#39;est pas spécifiée ou si elle est vide.

## Voir aussi {#section-5451b0525ed74121950bfc34726c3970}

[attribut::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
