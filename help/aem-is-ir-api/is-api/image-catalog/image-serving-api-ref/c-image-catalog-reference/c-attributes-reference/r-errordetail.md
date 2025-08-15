---
description: Détails du message d’erreur. Spécifie le niveau de détail des messages d’erreur renvoyés par HTTP en tant que valeur error.message.
solution: Experience Manager
title: Détail de l’erreur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 4%

---

# Détail de l’erreur{#errordetail}

Détails du message d’erreur. Spécifie le niveau de détail des messages d’erreur renvoyés par HTTP en tant que valeur error.message.

Les valeurs suivantes sont autorisées :

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Titre uniquement. Renvoie une brève description générale de l’erreur. Elle est recommandée pour les serveurs en direct accessibles publiquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Message bref. Réservé en vue d’une utilisation ultérieure. Renvoie actuellement les mêmes informations que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Message détaillé. Fournit des détails au niveau utilisateur sur l’erreur. Peut contenir des informations sensibles, telles que des chemins d’accès à des fichiers. Recommandé pour les serveurs intermédiaires, d’assurance qualité et de développement d’applications. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informations complètes sur le débogage. Ajoute les traces de la pile Java, le cas échéant. Les images d’erreur n’incluent jamais les traces de pile et renvoient plutôt des informations de niveau 2 dans <span class="codeph"> $error.message</span>. Ces informations peuvent être utiles pour signaler des problèmes au support technique Dynamic Media. </p></td> 
 </tr> 
</table>

## Propriétés {#section-e167895723ca4ad4ba283d3d7b4324de}

Valeur énumérée, doit être égale à 0, 1, 2 ou 3.

## Par défaut {#section-8f27098e509945a18676aca0675c8f41}

Hérité de `default::ErrorDetail` si elle n’est pas spécifiée ou si vide.

## Voir aussi {#section-5451b0525ed74121950bfc34726c3970}

[attribute ::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
