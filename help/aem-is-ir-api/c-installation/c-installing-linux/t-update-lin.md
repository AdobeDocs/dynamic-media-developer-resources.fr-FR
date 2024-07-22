---
title: Mise à jour à partir de IS 4.7.4 ou version ultérieure
description: Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Mise à jour à partir de IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving sous Linux®.

Si vous effectuez une mise à niveau à partir d’une ancienne version du serveur d’images, veuillez contacter l’assistance technique pour le processus approprié.

Le dossier [!DNL webapps] peut être supprimé lors de la mise à niveau. Sauvegardez le dossier [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à l’hôte de votre serveur avec les privilèges racine.
1. Décompressez et décompressez le fichier tar de distribution du serveur d’images.
1. Dans le dossier [!DNL setup], exécutez [!DNL `./install-is`] pour lancer l’assistant d’installation.

   Le programme d’installation de la mise à jour vérifie l’intégrité et la version du package installé. En cas de réussite, le contrat de licence de l’utilisateur final (&quot;EULA&quot;) s’affiche.
1. Lisez le contrat de licence, puis saisissez **[!UICONTROL y]** pour poursuivre l’installation.

   Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le dossier [!DNL BACKUP/].

   Une fois l’installation terminée, le message suivant s’affiche :

   `Image Server was started successfully`

Lors d’une mise à jour, le fichier [!DNL ImageServing/conf/server.xml] est mis à jour vers les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre [!DNL server.xml] existant et réimplémentez vos modifications après la mise à niveau.

Après une installation de mise à jour, envisagez de réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Pour plus d’informations, voir la description de l’utilitaire [!DNL playlog] .
