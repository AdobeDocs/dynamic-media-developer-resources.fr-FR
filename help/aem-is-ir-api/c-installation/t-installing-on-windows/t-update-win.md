---
description: Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving.
solution: Experience Manager
title: Mise à jour depuis IS 4.7.4 ou version ultérieure
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Mise à jour à partir de IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance technique pour connaître le processus approprié.

>[!NOTE]
>
>Le dossier [!DNL webapps] peut être supprimé lors de la mise à niveau. Sauvegardez le dossier [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à l’hôte du serveur avec des privilèges d’administration.
1. Extrayez le contenu du fichier compressé de distribution Image Serving.
1. Exécutez setup/setup.exe pour lancer l’assistant d’installation.
1. Cliquez sur **[!UICONTROL Suivant]** pour passer au contrat de licence de l’utilisateur final (CLUF), lisez le contrat de licence, puis cliquez sur **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour début l’installation de la mise à jour.

   >[!NOTE]
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le dossier [!DNL BACKUP/].

1. Une fois l&#39;installation terminée, cliquez sur &quot;Terminer&quot; pour quitter l&#39;assistant d&#39;installation.

   Dans certains cas, l&#39;assistant d&#39;installation peut demander de redémarrer le système.

Lors d’une mise à jour, le fichier [!DNL ImageServing/conf/server.xml] est mis à jour avec les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre [!DNL server.xml] existant et réimplémentez vos modifications après la mise à niveau.

Après une installation de mise à jour, pensez à réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Consultez la description de l&#39;utilitaire `playlog` pour plus d&#39;informations.
