---
title: Mise à jour à partir d’IS 4.7.4 ou version ultérieure
description: Suivez cette procédure lors de la mise à niveau de Dynamic Media serveur d’images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Mise à jour à partir d’IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Dynamic Media serveur d’images.

Si vous effectuez une mise à niveau à partir d’une ancienne version d’Image Server, veuillez contacter le support technique pour connaître le processus correct.

>[!NOTE]
>
>Le dossier peut être supprimé lors de la [!DNL webapps] mise à niveau. Sauvegardez le dossier avant la [!DNL webapps] mise à niveau.

1. Connectez-vous à votre hôte de serveur avec des droits d’administrateur.
1. Extract le contenu du fichier compressé de distribution Image Server.
1. Launch l’Assistant d’installation en exécutant `setup/setup.exe`.
1. Sélectionnez **[!UICONTROL Suivant]** pour accéder au Contrat de licence utilisateur final (CLUF), lisez le contrat de licence, puis sélectionnez **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour démarrer l’installation de la mise à jour.

   >[!NOTE]
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le [!DNL BACKUP/] dossier.

1. Une fois l’installation terminée, sélectionnez **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.

   Parfois, l’assistant d’installation peut vous demander de redémarrer le système.

Lors d’une mise à jour, le [!DNL ImageServing/conf/server.xml] fichier est mis à jour avec les paramètres les plus récents. Si vous avez modifié ou ajouté des valeurs, vous devez enregistrer vos modifications existantes [!DNL server.xml] et les réimplémenter après la mise à niveau.

Après l’installation d’une mise à jour, envisagez de réchauffer le cache de réponses HTTP avant de mettre le serveur en ligne. Reportez-vous à la description de l’utilitaire `playlog` pour plus de détails.
