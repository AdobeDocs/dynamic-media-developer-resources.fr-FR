---
description: Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving.
solution: Experience Manager
title: Mise à jour à partir de IS 4.7.4 ou version ultérieure
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Mise à jour à partir de IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving.

Si vous effectuez une mise à niveau à partir d’une ancienne version du serveur d’images, veuillez contacter l’assistance technique pour le processus approprié.

>[!NOTE]
>
>Le dossier [!DNL webapps] peut être supprimé lors de la mise à niveau. Sauvegardez le dossier [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à l’hôte de votre serveur avec les droits d’administrateur.
1. Extrayez le contenu du fichier zip de distribution Image Serving .
1. Exécutez setup/setup.exe pour lancer l’assistant d’installation.
1. Cliquez sur **[!UICONTROL Suivant]** pour accéder au contrat de licence de l’utilisateur final (EULA), lisez le contrat de licence, puis cliquez sur **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour lancer l’installation de la mise à jour.

   >[!NOTE]
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le dossier [!DNL BACKUP/].

1. Une fois l&#39;installation terminée, cliquez sur &quot;Terminer&quot; pour quitter l&#39;assistant d&#39;installation.

   Dans certains cas, l’assistant d’installation peut vous demander de redémarrer le système.

Lors d’une mise à jour, le fichier [!DNL ImageServing/conf/server.xml] est mis à jour vers les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre [!DNL server.xml] existant et réimplémentez vos modifications après la mise à niveau.

Après une installation de mise à jour, envisagez de réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Pour plus d’informations, voir la description de l’utilitaire `playlog` .
