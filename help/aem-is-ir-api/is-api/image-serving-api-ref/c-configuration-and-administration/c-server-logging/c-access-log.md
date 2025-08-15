---
description: Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées à l’ [!DNL Platform Server]. Si l’option Rendu d’image est activée, ses données de journal d’accès sont écrites dans le même fichier.
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

Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au [!DNL Platform Server]. Si l’option Rendu d’image est activée, ses données de journal d’accès sont écrites dans le même fichier.

Le journal d’accès est configuré dans server.xml.

>[!NOTE]
>
>Outre le trafic client pour la Diffusion d’images ( [!DNL /is/image/*]) et le Rendu d’images ( [!DNL /ir/render/*]), le journal d’accès peut inclure certains trafics internes : accès au système de catalogue [!DNL Platform Server] ( [!DNL /is-catalog/*]), partage du cache et demandes de redirection d’erreur ( [!DNL /is/cache/*]), accès à d’autres packages déployés sur l’[!DNL Platform Server], comme les visionneuses Dynamic Media ( [!DNL /is-viewers/*]), trafic statique et demandes de contenu statique traitées par l’[!DNL Platform Server] (par exemple, [!DNL /is-docs/*]).

Les requêtes avec des chemins d’accès racine [!DNL /is-catalog] et [!DNL /is/cache] doivent toujours être exclues de toute analyse du trafic client.
