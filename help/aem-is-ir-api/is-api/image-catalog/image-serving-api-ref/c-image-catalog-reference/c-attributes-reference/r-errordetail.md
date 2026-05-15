---
description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés par le biais du protocole HTTP comme valeur error.message.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
TQID: 'https://experienceleague.adobe.com/CZ2k-H1kZI3t3ZAtgm7qj8eo97u4NPmumdErNU--uvU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 4%

---

# ErrorDetail{#errordetail}

Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés par le biais du protocole HTTP comme valeur error.message.

Les valeurs suivantes sont autorisées :

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Titre uniquement. Renvoie une brève description générale de l’erreur. Recommandé pour les serveurs en ligne accessibles au public. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Message bref. Réservé à une utilisation ultérieure. Renvoie actuellement les mêmes informations que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Message détaillé. Fournit des détails au niveau de l’utilisateur sur l’erreur. Peut inclure des informations sensibles, telles que des chemins d’accès aux fichiers. Recommandé pour les serveurs d’évaluation, d’assurance qualité et de développement d’applications. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informations complètes de débogage. Ajoute des traces de pile Java, le cas échéant. Les images d’erreur n’incluent jamais de traces de pile et renvoient plutôt des informations de niveau 2 dans <span class="codeph"> $error.message</span>. Ces informations peuvent s’avérer utiles lors de la notification de problèmes au support technique de Dynamic Media. </p></td> 
 </tr> 
</table>

## Propriétés {#section-e167895723ca4ad4ba283d3d7b4324de}

La valeur énumérée doit être 0, 1, 2 ou 3.

## Par défaut {#section-8f27098e509945a18676aca0675c8f41}

Hérité de `default::ErrorDetail` si non spécifié ou si vide.

## Voir aussi {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
