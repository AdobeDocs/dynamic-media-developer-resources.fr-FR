---
description: Utilisez ces paramètres du serveur pour rediriger les erreurs.
solution: Experience Manager
title: Redirection d’erreur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Redirection d’erreur{#error-redirection}

Utilisez ces paramètres du serveur pour rediriger les erreurs.

>[!NOTE]
>
>Les caractères de barre verticale (|) du chemin suivant ne sont pas pris en charge pour la redirection des erreurs.

## PS::errorRedirect.rootUrl - Serveur de redirection {#section-85f22e48d68842a490b0e1191543b558}

L’URL racine ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) du déploiement secondaire du service d’images vers lequel les requêtes qui échouent localement doivent être redirigées. La redirection d’erreur est désactivée (par défaut) lorsque ce paramètre est vide ou non défini.

## PS::errorRedirect.connectTimeout - Délai d’expiration de la connexion de redirection {#section-3971be8f720d4b32a2cc7860b4085971}

Durée maximale (en ms) pendant laquelle le serveur attend qu’une connexion avec le serveur secondaire soit établie avant de renvoyer une erreur au client.

## PS::errorRedirect.socketTimeout - Délai d’expiration de la réponse de redirection {#section-69d8579f748d4044bca99dfb64dd523c}

Durée maximale (en ms) pendant laquelle le serveur secondaire attend le retour des données du serveur avant d’abandonner la demande de redirection et de renvoyer une erreur au client.
