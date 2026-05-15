---
description: Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des profils ICC et des macros de commande.
solution: Experience Manager
title: Catalogues d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Catalogues d’images{#image-catalogs}

Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des profils ICC et des macros de commande.

Ils mappent les identifiants d’image et de contenu statique utilisés dans les requêtes aux chemins d’accès de fichiers réels, stockent diverses métadonnées d’image, telles que les zones cliquables, et fournissent des conteneurs pour les modèles et les visionneuses d’images.

Les catalogues d’images ne sont accessibles que par le [!DNL Platform Server], et jamais par le serveur d’images. Les fichiers d’attributs de catalogue doivent comporter un suffixe .ini et être placés dans le dossier de catalogue du [!DNL Platform Server] ( `PS::CatalogFolder`). Le catalogue d’images par défaut est au moins obligatoire et doit être renseigné avec tous les attributs pour un fonctionnement correct du [!DNL Platform Server].
