---
description: Détails du message d’erreur. Indique le niveau de détail des messages d’erreur renvoyés via HTTP en tant que valeur error.message.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 5%

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
  <td class="stentry"> <p>Message détaillé. Fournit des détails sur l’erreur au niveau de l’utilisateur. Peut inclure des informations sensibles, telles que les chemins d’accès aux fichiers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informations complètes sur le débogage. Ajoute les traces de la pile Java, le cas échéant. Les images d’erreur n’incluent jamais de traces de pile et renvoient à la place des informations de niveau 2 dans <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Le niveau 0 est recommandé pour les serveurs actifs accessibles au public.
* Le niveau 2 est recommandé pour les serveurs d’évaluation, d’assurance de la qualité et de développement d’applications.
* Les informations de niveau 3 peuvent être utiles lorsque des problèmes de rapports au support technique Dynamic Media.

## Propriétés {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Valeur énumérée : 0, 1, 2 ou 3.

## Par défaut {#section-5e78d550050840cc9a1de811c581b94f}

Hérité de `default::ErrorDetail` si elle n&#39;est pas spécifiée ou si elle est vide.

## Voir aussi {#section-474e71922d194c7ca06f2aad3b30e025}

[attribut::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
