---
description: Si une requête ne peut pas être effectuée correctement, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.
solution: Experience Manager
title: Erreurs
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# Erreurs{#errors}

Si une requête ne peut pas être effectuée correctement, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.

La valeur de l’état de la réponse dépend du type de l’erreur. Pour les erreurs les plus courantes, il s’agit de &quot;403&quot;. Les réponses d’erreur pour les types de requêtes autres que les images sont conformes au format spécifié par `req=`. (Ne peut pas être mis en oeuvre de manière cohérente à l’heure actuelle.)

La quantité de détails incluse dans le message d’erreur peut être configurée avec `attribute::ErrorDetail`.

## Images d’erreur {#section-92e9b20b2507433daa96923abc95f777}

La diffusion d’images peut être configurée pour renvoyer les messages d’erreur rendus dans une image.

Voir [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) dans la référence du catalogue d’images pour plus de détails.

Si l’image d’erreur est générée, l’état de la réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse d’erreur HTTP standard et le message texte sont renvoyés au client.

## Image par défaut {#section-66bf25fe6b434081bfae96d38d9be25e}

La diffusion d’images peut être configurée pour remplacer une image manquante par une image par défaut. L’image par défaut peut être spécifiée avec `attribute::DefaultImage` ou le `defaultImage=` .

## Voir aussi {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
