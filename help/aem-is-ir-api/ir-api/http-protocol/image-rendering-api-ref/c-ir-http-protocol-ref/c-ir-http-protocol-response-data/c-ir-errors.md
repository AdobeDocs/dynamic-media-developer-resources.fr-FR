---
title: Erreurs
description: Si une requête ne peut pas être effectuée correctement, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# Erreurs{#errors}

Si une requête ne peut pas être effectuée correctement, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.

La valeur de l’état de la réponse dépend du type de l’erreur. pour la plupart des erreurs courantes, il s’agit de &quot;403&quot;. Les réponses d’erreur pour les types de requêtes autres que les images sont conformes au format spécifié par `req=`. (Il se peut que la mise en oeuvre ne soit pas cohérente actuellement.)

La quantité de détails incluse dans le message d’erreur peut être configurée avec `attribute::ErrorDetail`.

**Images d’erreur**

La diffusion d’images peut être configurée pour renvoyer les messages d’erreur rendus dans une image. Voir `attribute::ErrorImage` dans la référence du catalogue d’images pour plus de détails. Si l’image d’erreur est générée, l’état de la réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse d’erreur HTTP standard et le message texte sont renvoyés au client.

**Voir aussi**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
