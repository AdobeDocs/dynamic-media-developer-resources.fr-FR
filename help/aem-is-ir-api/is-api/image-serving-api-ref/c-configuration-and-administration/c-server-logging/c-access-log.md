---
description: Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées à l’ [!DNL Platform Server]. Si l’option Rendu d’image est activée, ses données de journal d’accès sont écrites dans le même fichier.
solution: Experience Manager
title: Journal d’accès
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# Journal d’accès{#access-log}

Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au [!DNL Platform Server]. Si l’option Rendu d’image est activée, ses données de journal d’accès sont écrites dans le même fichier.

Le journal d’accès est configuré dans server.xml.

>[!NOTE]
>
>Outre le trafic client pour la Diffusion d’images ( [!DNL /is/image/*]) et le Rendu d’images ( [!DNL /ir/render/*]), le journal d’accès peut inclure certains trafics internes : accès au système de catalogue [!DNL Platform Server] ( [!DNL /is-catalog/*]), partage du cache et demandes de redirection d’erreur ( [!DNL /is/cache/*]), accès à d’autres packages déployés sur l’[!DNL Platform Server], comme les visionneuses Dynamic Media ( [!DNL /is-viewers/*]), trafic statique et demandes de contenu statique traitées par l’[!DNL Platform Server] (par exemple, [!DNL /is-docs/*]).

Les requêtes avec des chemins d’accès racine [!DNL /is-catalog] et [!DNL /is/cache] doivent toujours être exclues de toute analyse du trafic client.
