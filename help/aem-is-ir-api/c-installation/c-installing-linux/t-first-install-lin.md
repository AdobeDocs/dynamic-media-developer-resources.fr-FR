---
description: Cette procédure explique comment installer Image Serving pour la première fois sous Linux.
seo-description: Cette procédure explique comment installer Image Serving pour la première fois sous Linux.
seo-title: Première installation
solution: Experience Manager
title: Première installation
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Première installation{#installing-for-the-first-time}

Cette procédure explique comment installer Image Serving pour la première fois sous Linux.

1. Connectez-vous à l’hôte du serveur avec les autorisations racine.
1. Créez le dossier [!DNL /usr/local/scene7/licenses].

   Si le fichier de clé de licence Image Serving et/ou Image Rendering (avec suffixe de [!DNL .sc8] fichier) est disponible, copiez-le dans ce dossier. Sinon, passez à l’installation et installez la clé de licence ultérieurement.
1. Décompressez et décompressez le fichier tar de distribution Image Serving.
1. 
   4. Exécutez [!DNL ./install-is], situé dans le [!DNL Setup] dossier, pour lancer l’assistant d’installation.
   Si aucune clé de licence n’est trouvée, des instructions s’affichent pour décrire comment obtenir un fichier de licence. Faites-le à ce stade ou poursuivez l’installation de la diffusion d’images et installez la clé de licence ultérieurement.
1. Lorsque le contrat de licence de l’utilisateur final (CLUF) s’affiche, lisez le contrat de licence, puis saisissez `y` pour continuer.

   Le programme d’installation affiche les invites répertoriées dans le tableau suivant.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Port d’écoute principal [8080] :</span> </p> </td> 
   <td colname="col2"> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Port d’écoute d’administrateur [8083] :</span> </p> </td> 
   <td colname="col2"> <p>Port d’écoute administrateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Taille maximale du cache HTTP (Mo) [2000] :</span> </p> </td> 
   <td colname="col2"> <p>Taille initiale du cache de réponse principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Dossier racine du cache [/usr/local/scene7/ImageServing/cache] :</span> </p> </td> 
   <td colname="col2"> <p>Dossier cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID du propriétaire du serveur d’images [racine] :</span> </p> </td> 
   <td colname="col2"> <p>compte utilisateur sous lequel les serveurs Image Serving doivent être installés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID de groupe du serveur d’images [racine] :</span> </p> </td> 
   <td colname="col2"> <p>Compte de groupe sous lequel les serveurs Image Serving doivent être installés. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Appuyez sur **[!UICONTROL Entrée]** pour accepter la valeur par défaut ou spécifier une autre valeur.

   Assurez-vous que tous les numéros de port spécifiés sont uniques et ne sont pas utilisés autrement sur cet hôte.

   **Important : **Si un compte autre que root est spécifié, vous devez vous assurer que les autorisations d’accès pour tous les fichiers et dossiers dont le serveur Image Server a besoin pour lire et/ou écrire sont correctement configurées lorsque ces dossiers sont reconfigurés dans les fichiers de configuration.
>Image Serving est maintenant installé sur [!DNL /usr/local/Scene7/ImageServing]. Certains contenus de rendu d’image sont installés sur [!DNL /usr/local/Scene7/ImageRendering].
>
>Vers la fin de l’installation, l’assistant d’installation tente de du serveur Image Server. Si aucune clé de licence valide n’est trouvée, le serveur Image Server ne peut pas . S’il existe une licence valide et que le serveur Image Server ne démarre toujours pas, consultez les fichiers journaux.
>[!NOTE]
Si la licence est installée après l’installation d’Image Serving, le serveur Image Server doit être démarré manuellement avant d’être utilisé.
>
>
>

