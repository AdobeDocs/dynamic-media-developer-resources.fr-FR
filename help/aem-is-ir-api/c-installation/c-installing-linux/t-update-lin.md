---
description: Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving sous Linux.
solution: Experience Manager
title: Mise à jour depuis IS 4.7.4 ou version ultérieure
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# Mise à jour à partir de IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Suivez cette procédure lors de la mise à niveau de Dynamic Media Image Serving sous Linux.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance technique pour connaître le processus approprié.

Le dossier [!DNL webapps] peut être supprimé lors de la mise à niveau. Veuillez sauvegarder le dossier [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à l’hôte du serveur avec les droits de root.
1. Décompressez et décompressez le fichier tar de distribution Image Serving.
1. Exécutez [!DNL ./install-is] pour lancer l&#39;assistant d&#39;installation situé dans le dossier [!DNL setup].

   Le programme d’installation de la mise à jour vérifie l’intégrité et la version du package installé. En cas de réussite, le contrat de licence de l’utilisateur final (&quot;CLUF&quot;) s’affiche.
1. Lisez le contrat de licence, puis saisissez &quot;**[!UICONTROL y]**&quot; pour poursuivre l’installation.

   Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le dossier [!DNL BACKUP/].

   Une fois l’installation terminée, le message suivant s’affiche :

   `Image Server was started successfully`

Lors d’une mise à jour, le fichier [!DNL ImageServing/conf/server.xml] est mis à jour avec les derniers paramètres. Si vous avez modifié ou ajouté des valeurs, enregistrez votre [!DNL server.xml] existant et réimplémentez vos modifications après la mise à niveau.

Après une installation de mise à jour, pensez à réchauffer le cache de réponse HTTP avant de mettre le serveur en service. Consultez la description de l&#39;utilitaire [!DNL playlog] pour plus d&#39;informations.
