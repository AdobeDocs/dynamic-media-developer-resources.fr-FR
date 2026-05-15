---
title: Mise à jour à partir d’IS 4.7.4 ou version ultérieure
description: Utilisez cette procédure lors de la mise à niveau de la diffusion d’images Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
TQID: 'https://experienceleague.adobe.com/ibeLWHpA-Lk2wiXkSgGL02uMEYH4t8l0xjjXuN9ooiE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 0%

---

# Mise à jour à partir d’IS 4.7.4 ou version ultérieure{#updating-from-is-or-later}

Utilisez cette procédure lors de la mise à niveau de la diffusion d’images Dynamic Media.

Si vous effectuez une mise à niveau à partir d’une ancienne version de la diffusion d’images, contactez l’assistance pour le processus approprié.

>[!NOTE]
>
>Le dossier [!DNL webapps] peut être supprimé lors de la mise à niveau. Sauvegardez le dossier [!DNL webapps] avant la mise à niveau.

1. Connectez-vous à votre hôte de serveur avec des droits d’administrateur.
1. Extrayez le contenu du fichier zip de distribution du service d’images.
1. Lancez l&#39;assistant d&#39;installation en exécutant `setup/setup.exe`.
1. Sélectionnez **[!UICONTROL Suivant]** pour accéder au contrat de licence de l’utilisateur final (CLUF), lisez le contrat de licence, puis sélectionnez **[!UICONTROL Oui]**.

   La page suivante affiche les paramètres de configuration précédents.
1. Cliquez sur **[!UICONTROL Suivant]** pour lancer l’installation de la mise à jour.

   >[!NOTE]
   >
   >Le programme d’installation sauvegarde les anciens fichiers de configuration du serveur dans le dossier [!DNL BACKUP/].

1. Une fois l’installation terminée, sélectionnez **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.

   Parfois, l&#39;assistant d&#39;installation peut vous demander de redémarrer le système.

Lors d’une mise à jour, le fichier [!DNL ImageServing/conf/server.xml] est mis à jour aux derniers paramètres. Si vous avez modifié ou ajouté des valeurs, vous devez enregistrer vos [!DNL server.xml] existantes et réimplémenter vos modifications après la mise à niveau.

Après une installation de mise à jour, envisagez de préchauffer le cache de réponse HTTP avant de mettre le serveur en ligne. Reportez-vous à la description de l’utilitaire `playlog` pour plus d’informations.
