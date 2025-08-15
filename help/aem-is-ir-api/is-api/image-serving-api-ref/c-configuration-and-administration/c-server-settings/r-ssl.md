---
description: Utilisez ces paramètres de serveur pour SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# SSL{#ssl}

Utilisez ces paramètres de serveur pour SSL.

## TC ::SslPort - Port d’écoute {#section-c80eb582bf684b3fa7313a77cc606769}

Spécifie le port d’écoute pour les [!DNL Platform Server] connexions SSL. Par défaut : 8443.

## TC ::keystoreFile - Chemin d’accès au fichier keystore {#section-0cdf9b3cfcf249818b22221d01bafebe}

Spécifiez le chemin/nom du fichier de stockage de clés SSL. Peut être un chemin absolu ou un chemin relatif à [!DNL *[!DNL install_folder]*/conf]. La valeur par défaut est *install_folder*/conf/scene7keystore.

## TC ::keystorePass - Mot de passe keystore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

mot de passe du fichier de stockage des clés. La valeur par défaut est `scene7`.

## TC ::keystoreType - Type de magasin de clés {#section-8f263e1ba67740728cd39181960d7c7d}

Sélectionnez le type de fichier de stockage des clés. `Java'` &#39; (par défaut) et &#39; `PKCS12`&#39; sont pris en charge.
