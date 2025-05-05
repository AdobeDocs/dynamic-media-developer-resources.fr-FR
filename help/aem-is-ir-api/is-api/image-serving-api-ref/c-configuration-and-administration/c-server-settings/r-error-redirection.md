---
description: Utilisez ces paramètres de serveur pour rediriger les erreurs.
solution: Experience Manager
title: Redirection des erreurs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Redirection des erreurs{#error-redirection}

Utilisez ces paramètres de serveur pour rediriger les erreurs.

>[!NOTE]
>
>Les caractères de pixel (|) dans le chemin d’accès net ne sont pas pris en charge pour la redirection d’erreur.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

L’URL racine ( HTTP:// *[!DNL domain]*[: *[!DNL port]*]) pour le déploiement de serveur d’images secondaire vers lequel les demandes qui échouent localement doivent être redirigées. La redirection d’erreur est désactivée (par défaut) lorsque ce paramètre est vide ou non défini.

## PS::errorRedirect.connectTimeout - Redirect Connection Timeout {#section-3971be8f720d4b32a2cc7860b4085971}

Délai maximum (en ms) pendant lequel le serveur attend qu’une connexion au serveur secondaire soit établie avant de renvoyer une erreur au client.

## PS::errorRedirect.socketTimeout - Redirect Response Timeout {#section-69d8579f748d4044bca99dfb64dd523c}

Délai maximum (en ms) pendant lequel le serveur attend que le serveur secondaire renvoie les données avant d’abandonner la demande de redirection et de renvoyer une erreur au client.
