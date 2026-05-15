---
title: Mise à jour à partir d’IS 4.7.4 ou version ultérieure
description: Utilisez cette procédure lors de la mise à niveau de la diffusion d’images Dynamic Media sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
TQID: 'https://experienceleague.adobe.com/RGRlIuemg6bPstlymZg7Ajr9i2ANq-HNjoIULaJydfs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 0%

---

# Mise à jour à partir d’IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Utilisez cette procédure lors de la mise à niveau de la diffusion d’images Dynamic Media sous Linux®.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance pour le processus approprié.

Le dossier [!DNL webapps] peut être supprimé lors de la mise à niveau. Sauvegardez le dossier [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à votre hôte serveur avec les privilèges root.
1. Décompressez et décompressez le fichier tar de distribution du service d’images.
1. Dans le dossier [!DNL setup], exécutez [!DNL `./install-is`] pour lancer l’assistant d’installation.

   Le programme d’installation de la mise à jour vérifie l’intégrité et la version du package installé. En cas de réussite, le contrat de licence de l’utilisateur final (« CLUF ») s’affiche.
1. Lisez le contrat de licence, puis entrez **[!UICONTROL y]** pour poursuivre l’installation.

   Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le dossier [!DNL BACKUP/].

   Une fois l’installation terminée, le message suivant s’affiche :

   `Image Server was started successfully`

Lors d’une mise à jour, le fichier [!DNL ImageServing/conf/server.xml] est mis à jour aux derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez vos [!DNL server.xml] existantes et implémentez à nouveau vos modifications après la mise à niveau.

Après une installation de mise à jour, envisagez de préchauffer le cache de réponse HTTP avant de mettre le serveur en ligne. Reportez-vous à la description de l’utilitaire [!DNL playlog] pour plus d’informations.
