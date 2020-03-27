---
description: Utilisez ces paramètres de serveur pour rediriger les erreurs.
seo-description: Utilisez ces paramètres de serveur pour rediriger les erreurs.
seo-title: Redirection d'erreur
solution: Experience Manager
title: Redirection d'erreur
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Redirection d&#39;erreur{#error-redirection}

Utilisez ces paramètres de serveur pour rediriger les erreurs.

>[!NOTE]
>
>Les caractères de tuyau (|) dans le chemin d’accès réseau ne sont pas pris en charge pour la redirection d’erreur.

## PS::errorRedirect.rootUrl - Serveur de redirection {#section-85f22e48d68842a490b0e1191543b558}

URL racine ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) pour le déploiement secondaire de la diffusion d’images auquel les demandes qui échouent localement doivent être redirigées. La redirection d’erreur est désactivée (par défaut) lorsque ce paramètre est vide ou non défini.

## PS::errorRedirect.connectTimeout - Délai de connexion de redirection {#section-3971be8f720d4b32a2cc7860b4085971}

Temps maximal (en msec) pendant lequel le serveur attend qu’une connexion avec le serveur secondaire soit établie avant de renvoyer une erreur au client.

## PS::errorRedirect.socketTimeout - Délai de réponse de redirection {#section-69d8579f748d4044bca99dfb64dd523c}

Délai maximal (en msec) pendant lequel le serveur secondaire attend que le serveur secondaire renvoie des données avant d’abandonner la requête de redirection et de renvoyer une erreur au client.
