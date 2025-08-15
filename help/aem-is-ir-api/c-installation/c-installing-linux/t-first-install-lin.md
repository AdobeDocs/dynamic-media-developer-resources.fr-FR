---
title: Première installation
description: Cette procédure montre comment installer Image Serving pour la première fois sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Première installation{#installing-for-the-first-time}

Cette procédure explique comment installer la diffusion d’images pour la première fois sous Linux®.

1. Connectez-vous à votre hôte serveur avec les autorisations root.
1. Créez le dossier [!DNL /usr/local/scene7/licenses].

   Si le fichier de clé de licence Image Serving et/ou Image Rendering (avec [!DNL .sc8] suffixe de fichier) est disponible, copiez-le dans ce dossier. Sinon, procédez à l’installation et installez la clé de licence ultérieurement.
1. Décompressez et décompressez le fichier tar de distribution Image Server.
1. Dans le [!DNL Setup] dossier, lancez l’assistant d’installation en exécutant [!DNL ./install-is].

   Si aucune clé de licence n’est trouvée, des instructions s’affichent décrivant comment obtenir un fichier de licence. Faites-le à ce stade ou poursuivez l’installation d’Image Serving et installez la clé de licence ultérieurement.
1. Lorsque le contrat de licence utilisateur final (CLUF) s’affiche, lisez le contrat de licence, puis entrez `y` pour continuer.

   Le programme d’installation affiche les invites répertoriées dans le tableau suivant.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> port d'écoute principal [8080]:</span> </p> </td>
   <td colname="col2"> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>Port D'Écoute D'Administration <span class="codeph"> [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Port d’écoute administrateur. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Taille maximale du cache HTTP (Mo) [2000] :</span> </p> </td> 
   <td colname="col2"> <p>Taille initiale du cache de réponse principal. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Dossier racine de cache [/usr/local/scene7/ImageServing/cache] :</span> </p> </td> 
   <td colname="col2"> <p>Dossier cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID du propriétaire du serveur d’images [racine] :</span> </p> </td>
   <td colname="col2"> <p>Compte utilisateur sous lequel le serveur Image Serving doit être installé. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p>ID de groupe de serveurs d’images <span class="codeph"> [root]:</span> </p> </td>
   <td colname="col2"> <p>Compte de groupe sous lequel le serveur de diffusion d’images doit être installé. </p> </td>
  </tr>
 </tbody>
</table>

1. Appuyez sur **[!UICONTROL Entrée]** pour accepter la valeur par défaut ou spécifier une autre valeur.

   Assurez-vous que tous les numéros de port spécifiés sont uniques et ne sont pas utilisés sur cet hôte.

   >[!IMPORTANT]
   >
   >Si un compte autre que root est spécifié, vous devez vous assurer que les autorisations d’accès pour tous les fichiers et dossiers que le serveur d’images doit lire et écrire sont correctement configurées lors de la reconfiguration de ces dossiers dans les fichiers de configuration.
   >
   >La diffusion d’images est maintenant installée sur [!DNL /usr/local/Scene7/ImageServing]. Certains contenus Image Rendering sont installés sur [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Vers la fin de l’installation, l’assistant d’installation tente de démarrer Image Server. Si aucune clé de licence valide n’est trouvée, le serveur d’images ne peut pas démarrer. S’il existe une licence valide et que Image Server ne démarre toujours pas, consultez les fichiers journaux.

>[!NOTE]
>
>Si la licence est installée après l’installation d’Image Server, le serveur d’images doit être démarré manuellement avant utilisation.
