---
title: Mise à jour à partir de IS 4.7.4 ou version ultérieure
description: Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Mise à jour à partir de IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving.

Si vous effectuez une mise à niveau à partir d’une ancienne version du serveur d’images, veuillez contacter l’assistance technique pour le processus approprié.

>[!NOTE]
>
>Le [!DNL webapps] peut être supprimé lors de la mise à niveau. Sauvegardez les [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à l’hôte de votre serveur avec les droits d’administrateur.
1. Extrayez le contenu du fichier zip de distribution Image Serving .
1. Lancez l’assistant d’installation en exécutant `setup/setup.exe`.
1. Sélectionner **[!UICONTROL Suivant]** pour accéder au contrat de licence de l’utilisateur final (EULA), lisez le contrat de licence, puis sélectionnez **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour lancer l&#39;installation de la mise à jour.

   >[!NOTE]
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le [!DNL BACKUP/] dossier.

1. Une fois l’installation terminée, sélectionnez **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.

   Parfois, l’assistant d’installation peut vous demander de redémarrer le système.

Lors d’une mise à jour, la variable [!DNL ImageServing/conf/server.xml] est mis à jour vers les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, vous devez enregistrer votre [!DNL server.xml] et réimplémentez vos modifications après la mise à niveau.

Après une installation de mise à jour, envisagez de réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Reportez-vous à la description du `playlog` pour plus d’informations.
