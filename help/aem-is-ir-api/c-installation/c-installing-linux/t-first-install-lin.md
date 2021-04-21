---
description: Cette procédure explique comment installer Image Serving pour la première fois sous Linux.
solution: Experience Manager
title: Première installation
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# Première installation de {#installing-for-the-first-time}

Cette procédure explique comment installer Image Serving pour la première fois sous Linux.

1. Connectez-vous à l’hôte du serveur avec les autorisations de la racine.
1. Créez le dossier [!DNL /usr/local/scene7/licenses].

   Si le fichier de clé de licence Image Serving et/ou Image Rendering (avec le suffixe de fichier [!DNL .sc8]) est disponible, copiez-le dans ce dossier. Sinon, passez à l’installation et installez la clé de licence ultérieurement.
1. Décompressez et décompressez le fichier tar de distribution Image Serving.
1. Exécutez [!DNL ./install-is], situé dans le dossier [!DNL Setup], pour lancer l’assistant d’installation.

   Si aucune clé de licence n’est trouvée, des instructions s’affichent pour décrire comment obtenir un fichier de licence. Faites-le à ce stade ou passez à l’installation de Image Serving et installez la clé de licence ultérieurement.
1. Lorsque le contrat de licence de l&#39;utilisateur final s&#39;affiche, lisez le contrat de licence, puis saisissez `y` pour continuer.

   Le programme d’installation affiche les invites répertoriées dans le tableau suivant.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Port d’écoute principal [8080] :</span> </p> </td> 
   <td colname="col2"> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Port d’écoute Admin [8083] :</span> </p> </td> 
   <td colname="col2"> <p>Admin port d’écoute. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Taille maximale du cache HTTP (Mo) [2000] :</span> </p> </td> 
   <td colname="col2"> <p>Taille initiale du cache de réponse principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Dossier racine du cache [/usr/local/scene7/ImageServing/cache] :</span> </p> </td> 
   <td colname="col2"> <p>dossier de cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID du propriétaire du serveur d’images [racine] :</span> </p> </td> 
   <td colname="col2"> <p>compte utilisateur sous lequel les serveurs Image Serving doivent être installés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID du groupe de serveurs d’images [racine] :</span> </p> </td> 
   <td colname="col2"> <p>Compte de groupe sous lequel les serveurs Image Serving doivent être installés. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Appuyez sur **[!UICONTROL Entrée]** pour accepter la valeur par défaut ou spécifier une autre valeur.

   Assurez-vous que tous les numéros de port spécifiés sont uniques et ne sont pas utilisés autrement sur cet hôte.

   >[!IMPORTANT]
   >
   >Si un compte autre que root est spécifié, vous devez vous assurer que les autorisations d’accès pour tous les fichiers et dossiers dont le serveur Image Server a besoin pour lire et/ou écrire sont correctement configurées lorsque ces dossiers sont reconfigurés dans les fichiers de configuration.
   >
   >Image Serving est maintenant installé sur [!DNL /usr/local/Scene7/ImageServing]. Certains contenus de rendu d’image sont installés dans [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Vers la fin de l’installation, l’assistant d’installation tente de début Image Server. Si aucune clé de licence valide n’est trouvée, le serveur Image Server ne peut pas être début. S’il existe une licence valide et qu’Image Server ne démarre toujours pas, consultez les fichiers journaux.

>[!NOTE]
>
>Si la licence est installée après l’installation d’Image Serving, le serveur Image Server doit être démarré manuellement avant d’être utilisé.
