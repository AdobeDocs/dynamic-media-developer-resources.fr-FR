---
title: Erreurs
description: Si une requête ne peut pas être exécutée correctement, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200, ainsi qu’un message d’erreur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
TQID: 'https://experienceleague.adobe.com/TSTpmfiuEppAPSUxX1ga5lfQSgWRkI2Wh1CXoalSU9A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# Erreurs{#errors}

Si une requête ne peut pas être exécutée correctement, le serveur renvoie une image d’erreur ou un état de réponse HTTP autre que 200, ainsi qu’un message d’erreur.

La valeur du statut de la réponse dépend du type de l’erreur ; pour les erreurs les plus courantes, elle est « 403 ». Les réponses d’erreur pour les types de requêtes autres que les requêtes d’image sont conformes au format spécifié avec `req=`. (n’est peut-être pas implémentée de manière cohérente actuellement.)

La quantité de détails inclus dans le message d’erreur est configurable avec `attribute::ErrorDetail`.

**Images d’erreur**

La diffusion d’images peut être configurée pour renvoyer des messages d’erreur générés dans une image. Voir `attribute::ErrorImage` dans la référence du catalogue d’images pour plus d’informations. Si l’image d’erreur est générée avec succès, l’état de la réponse HTTP est 200. Si une erreur se produit lors du traitement de l’image d’erreur, la réponse d’erreur HTTP standard et le message texte sont renvoyés au client.

**Voir aussi**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)

