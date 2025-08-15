---
description: Si une demande ne peut pas être effectuée avec succès, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.
solution: Experience Manager
title: Erreurs
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Erreurs{#errors}

Si une demande ne peut pas être effectuée avec succès, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200 avec un message d’erreur.

La valeur de l’état de réponse dépend du type de l’erreur ; pour la plupart des erreurs courantes, il s’agit de « 403 ». Les réponses d’erreur pour les types de demandes autres que les images sont conformes au format spécifié avec `req=`. (Peut ne pas être mis en œuvre de manière cohérente à l’heure actuelle.)

La quantité de détails incluse dans le message d’erreur peut être configurée avec `attribute::ErrorDetail`.

## Images d’erreur {#section-92e9b20b2507433daa96923abc95f777}

La diffusion d’images peut être configurée pour renvoyer les messages d’erreur rendus dans une image.

Pour plus d’informations, voir [attribute ::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) dans la référence du catalogue d’images.

Si l’image d’erreur est générée avec succès, l’état de réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse d’erreur HTTP standard et le message texte sont renvoyés au client.

## Image par défaut {#section-66bf25fe6b434081bfae96d38d9be25e}

La diffusion d’images peut être configurée pour remplacer une image manquante par une image par défaut. L’image par défaut peut être spécifiée à l’aide de la commande ou à l’aide `attribute::DefaultImage` de la `defaultImage=` commande.

## Voir aussi {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute ::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute ::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute ::D efaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
