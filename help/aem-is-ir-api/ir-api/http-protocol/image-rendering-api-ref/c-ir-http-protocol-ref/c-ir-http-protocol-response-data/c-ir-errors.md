---
title: Erreurs
description: Si une demande ne peut pas être effectuée avec succès, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Erreurs{#errors}

Si une demande ne peut pas être effectuée avec succès, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.

La valeur de l’état de réponse dépend du type de l’erreur ; pour la plupart des erreurs courantes, il s’agit de « 403 ». Les réponses d’erreur pour les types de demandes autres que les images sont conformes au format spécifié avec `req=`. (Peut ne pas être implémenté de manière cohérente actuellement.)

La quantité de détails incluse dans le message d’erreur peut être configurée avec `attribute::ErrorDetail`.

**Images d’erreur**

La diffusion d’images peut être configurée pour renvoyer les messages d’erreur rendus dans une image. Voir `attribute::ErrorImage` dans le catalogue d’images référence pour plus de détails. Si l’image d’erreur est générée avec succès, l’état de réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse d’erreur HTTP standard et le message texte sont renvoyés au client.

**Voir aussi**

[attribute ::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute ::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
