---
description: Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au [!DNL Platform Server]. S’il est activé, le rendu d’image écrit ses données de journal d’accès dans le même fichier.
solution: Experience Manager
title: Journal d’accès
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Journal d’accès{#access-log}

Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au [!DNL Platform Server]. S’il est activé, le rendu d’image écrit ses données de journal d’accès dans le même fichier.

Le journal des accès est configuré dans server.xml.

>[!NOTE]
>
>Outre le trafic client pour la diffusion d’images ( [!DNL /is/image/*]) et rendu d’image ( [!DNL /ir/render/*]), le journal des accès peut contenir un certain trafic interne : accès au [!DNL Platform Server] système de catalogue ( [!DNL /is-catalog/*]), partage du cache et demandes de redirection d’erreur ( [!DNL /is/cache/*]), accès aux autres modules déployés sur le [!DNL Platform Server], comme les visionneuses Dynamic Media ( [!DNL /is-viewers/*]), les demandes de trafic statique et de contenu statique traitées par le [!DNL Platform Server] (par exemple, [!DNL /is-docs/*]).

Requêtes avec [!DNL /is-catalog] et [!DNL /is/cache] les chemins racine doivent toujours être exclus de toute analyse du trafic client.
