---
title: Mise à jour à partir d’IS 4.7.4 ou version ultérieure
description: Utilisez cette procédure lors de la mise à niveau de la diffusion d’images Dynamic Media sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '206'
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
