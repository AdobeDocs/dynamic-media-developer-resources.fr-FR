---
description: Le catalogue par défaut fournit les valeurs par défaut de tous les attributs de catalogue pour tous les catalogues d’images.
solution: Experience Manager
title: Catalogue par défaut
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# Catalogue par défaut{#default-catalog}

Le catalogue par défaut fournit les valeurs par défaut de tous les attributs de catalogue pour tous les catalogues d’images.

Si un attribut particulier est introuvable dans un catalogue d’images spécifique, le serveur utilise la valeur correspondante du catalogue par défaut à la place. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (images, définitions de macro, polices et profils ICC). Si un enregistrement de données spécifique est introuvable dans un catalogue d’images spécifique, le serveur tente de le trouver dans le catalogue par défaut à la place. Cela permet de renseigner les catalogues d’images de manière éparse et de simplifier la gestion des attributs et des données globaux, tels que les modèles partagés, les macros, les polices, etc.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (macros, polices, profils ICC, règles de pré-traitement des demandes) lorsqu’aucun catalogue d’images spécifique n’est impliqué dans une opération.

Pour le bon fonctionnement du [!DNL Platform Server], le fichier d’attributs de catalogue du catalogue par défaut doit être nommé [!DNL default.ini], doit toujours exister dans le dossier de catalogue et doit être entièrement renseigné avec tous les attributs requis, à l’exclusion des `attribute::RootId` et des références aux différents fichiers de données de catalogue, qui sont tous facultatifs.

>[!NOTE]
>
>Tous les fichiers d’attributs de catalogue, à l’exception de [!DNL default.ini], doivent contenir une valeur `attribute::RootId` unique. `attribute::RootId` dans [!DNL default.ini] doit être vide.
