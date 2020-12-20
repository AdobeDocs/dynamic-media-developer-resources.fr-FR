---
description: Si une requête ne peut pas être traitée correctement, le serveur renvoie soit une image d'erreur, soit un état de réponse HTTP autre que 200 avec un message d'erreur.
seo-description: Si une requête ne peut pas être traitée correctement, le serveur renvoie soit une image d'erreur, soit un état de réponse HTTP autre que 200 avec un message d'erreur.
seo-title: Erreurs
solution: Experience Manager
title: Erreurs
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# Erreurs{#errors}

Si une requête ne peut pas être traitée correctement, le serveur renvoie soit une image d&#39;erreur, soit un état de réponse HTTP autre que 200 avec un message d&#39;erreur.

La valeur d’état de la réponse dépend du type de l’erreur ; pour la plupart des erreurs courantes, il s&#39;agit de &quot;403&quot;. Les réponses d’erreur pour les types de requêtes autres que les demandes d’image sont conformes au format spécifié par `req=`. (Peut-être ne pas être mis en oeuvre de manière cohérente pour le moment.)

La quantité de détails incluse dans le message d&#39;erreur peut être configurée avec `attribute::ErrorDetail`.

**Images d’erreur**

La diffusion d’images peut être configurée pour renvoyer des messages d’erreur générés dans une image. Voir `attribute::ErrorImage` dans la référence du catalogue d’images pour plus d’informations. Si l’image d’erreur est générée avec succès, l’état de la réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse HTTP standard et le message texte sont renvoyés au client.

**Voir aussi**

[attribut::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribut::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
