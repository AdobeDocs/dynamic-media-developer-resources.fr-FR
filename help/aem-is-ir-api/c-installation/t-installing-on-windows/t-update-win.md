---
description: Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving.
seo-description: Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving.
seo-title: Mise à jour depuis IS 4.7.4 ou version ultérieure
solution: Experience Manager
title: Mise à jour depuis IS 4.7.4 ou version ultérieure
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Mise à jour depuis IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance technique pour connaître le processus approprié.

>[!NOTE]
>
>Le [!DNL webapps] dossier peut être supprimé lors de la mise à niveau. Sauvegardez le [!DNL webapps] dossier avant la mise à niveau.

1. Connectez-vous à l’hôte du serveur avec des privilèges d’administration.
1. Extrayez le contenu du fichier compressé de distribution Image Serving.
1. Exécutez setup/setup.exe pour lancer l’assistant d’installation.
1. Cliquez sur **[!UICONTROL Suivant]** pour passer au contrat de licence de l’utilisateur final (CLUF), lisez le contrat de licence et cliquez sur **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour début de l’installation de la mise à jour.

   >[!NOTE]
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le [!DNL BACKUP/] dossier.

1. Une fois l&#39;installation terminée, cliquez sur &quot;Terminer&quot; pour quitter l&#39;assistant d&#39;installation.

   Dans certains cas, l&#39;assistant d&#39;installation peut demander de redémarrer le système.
>Lors d’une mise à jour, le [!DNL ImageServing/conf/server.xml] fichier est mis à jour avec les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre fichier existant [!DNL server.xml] et réimplémentez vos modifications après la mise à niveau.
>
>Après une installation de mise à jour, pensez à réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Pour plus d&#39;informations, reportez-vous à la description de l&#39; `playlog` utilitaire.

