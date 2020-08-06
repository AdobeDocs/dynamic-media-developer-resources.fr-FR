---
description: Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving sous Linux.
seo-description: Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving sous Linux.
seo-title: Mise à jour depuis IS 4.7.4 ou version ultérieure
solution: Experience Manager
title: Mise à jour depuis IS 4.7.4 ou version ultérieure
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 038f0f8f2c4f815e47749e0bab153c63e5396c91
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Mise à jour depuis IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Scene7 Image Serving sous Linux.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance technique pour connaître le processus approprié.

Le [!DNL webapps] dossier peut être supprimé lors de la mise à niveau. Effectuez une sauvegarde du [!DNL webapps] dossier avant la mise à niveau.

1. Connectez-vous à l’hôte du serveur avec les droits de root.
1. Décompressez et décompressez le fichier tar de distribution Image Serving.
1. Exécutez [!DNL ./install-is] pour lancer l’assistant d’installation situé dans le [!DNL setup] dossier.

   Le programme d’installation de la mise à jour vérifie l’intégrité et la version du package installé. En cas de réussite, le contrat de licence de l’utilisateur final (&quot;CLUF&quot;) s’affiche.
1. Lisez le contrat de licence, puis saisissez &quot; **[!UICONTROL y]**&quot; pour poursuivre l’installation.

   Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le [!DNL BACKUP/] dossier.

   Une fois l’installation terminée, le message suivant s’affiche :

   `Image Server was started successfully`

Lors d’une mise à jour, le [!DNL ImageServing/conf/server.xml] fichier est mis à jour avec les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre fichier existant [!DNL server.xml] et réimplémentez vos modifications après la mise à niveau.

Après une installation de mise à jour, pensez à réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Pour plus d&#39;informations, reportez-vous à la description de l&#39; [!DNL playlog] utilitaire.
