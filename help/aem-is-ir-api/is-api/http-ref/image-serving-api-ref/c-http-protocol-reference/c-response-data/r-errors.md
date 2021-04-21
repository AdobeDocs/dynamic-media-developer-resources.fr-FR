---
description: Si une requête ne peut pas être traitée correctement, le serveur renvoie soit une image d'erreur, soit un état de réponse HTTP autre que 200 avec un message d'erreur.
solution: Experience Manager
title: Erreurs
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---


# Erreurs{#errors}

Si une requête ne peut pas être traitée correctement, le serveur renvoie soit une image d&#39;erreur, soit un état de réponse HTTP autre que 200 avec un message d&#39;erreur.

La valeur d’état de la réponse dépend du type de l’erreur ; pour la plupart des erreurs courantes, il s&#39;agit de &quot;403&quot;. Les réponses d’erreur pour les types de requêtes autres que les demandes d’image sont conformes au format spécifié par `req=`. (Peut ne pas être mis en oeuvre de manière cohérente pour le moment.)

La quantité de détails incluse dans le message d&#39;erreur peut être configurée avec `attribute::ErrorDetail`.

## Images d&#39;erreur {#section-92e9b20b2507433daa96923abc95f777}

La diffusion d’images peut être configurée pour renvoyer des messages d’erreur générés dans une image.

Voir [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) dans la référence du catalogue d’images pour plus d’informations.

Si l’image d’erreur est générée avec succès, l’état de la réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse HTTP standard et le message texte sont renvoyés au client.

## Image par défaut {#section-66bf25fe6b434081bfae96d38d9be25e}

La diffusion d’images peut être configurée pour remplacer une image manquante par une image par défaut. L&#39;image par défaut peut être spécifiée soit avec `attribute::DefaultImage`, soit avec la commande `defaultImage=`.

## Voir aussi {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribut::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ,  [attribut::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribut::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
