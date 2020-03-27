---
description: Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving.
seo-description: Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving.
seo-title: Mise à jour depuis IS 4.7.4 ou version ultérieure
solution: Experience Manager
title: Mise à jour depuis IS 4.7.4 ou version ultérieure
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mise à jour depuis IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance technique pour connaître le processus approprié.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le [!DNL webapps] dossier peut être supprimé lors de la mise à niveau. Sauvegardez le [!DNL webapps] dossier avant la mise à niveau.

1. Connectez-vous à l’hôte du serveur avec des privilèges d’administrateur.
1. Extrayez le contenu du fichier .zip de distribution Image Serving.
1. Exécutez setup/setup.exe pour lancer l’assistant d’installation.
1. Cliquez sur **[!UICONTROL Suivant]** pour accéder au contrat de licence de l’utilisateur final (CLUF), lisez le contrat de licence, puis cliquez sur **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour de l’installation de la mise à jour.

   >[!NOTE] {class=&quot;- rubrique/note &quot;}
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le [!DNL BACKUP/] dossier.

1. Une fois l’installation terminée, cliquez sur &quot;Terminer&quot; pour quitter l’assistant d’installation.

   Dans certains cas, l&#39;assistant d&#39;installation peut demander de redémarrer le système.
>Lors d’une mise à jour, le [!DNL ImageServing/conf/server.xml] fichier est mis à jour avec les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre fichier existant [!DNL server.xml] et réimplémentez vos modifications après la mise à niveau.
>
>Après une installation de mise à jour, pensez à réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Consultez la description de l&#39; `playlog` utilitaire pour plus de détails.

