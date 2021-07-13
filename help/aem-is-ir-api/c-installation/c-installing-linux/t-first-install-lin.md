---
description: Cette procédure explique comment installer Image Serving pour la première fois sous Linux.
solution: Experience Manager
title: Première installation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Première installation{#installing-for-the-first-time}

Cette procédure explique comment installer Image Serving pour la première fois sous Linux.

1. Connectez-vous à l’hôte du serveur avec les autorisations racine.
1. Créez le dossier [!DNL /usr/local/scene7/licenses].

   Si le fichier de clé de licence Image Serving et/ou Image Rendering (avec le suffixe de fichier [!DNL .sc8]) est disponible, copiez-le dans ce dossier. Sinon, passez à l’installation et installez la clé de licence ultérieurement.
1. Décompressez et décompressez le fichier tar de distribution du serveur d’images.
1. Exécutez [!DNL ./install-is], situé dans le dossier [!DNL Setup], pour lancer l’assistant d’installation.

   Si aucune clé de licence n’est trouvée, des instructions décrivant comment obtenir un fichier de licence s’affichent. À ce stade, effectuez l’installation du serveur d’images et installez la clé de licence ultérieurement.
1. Lorsque le contrat de licence de l’utilisateur final s’affiche, lisez le contrat de licence, puis saisissez `y` pour continuer.

   Le programme d’installation affiche les invites répertoriées dans le tableau suivant.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Port d'écoute principal [8080] :</span> </p> </td> 
   <td colname="col2"> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Port d’écoute d’administrateur [8083] :</span> </p> </td> 
   <td colname="col2"> <p>Port d’écoute de l’administrateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Taille maximale du cache HTTP (Mo) [2 000] :</span> </p> </td> 
   <td colname="col2"> <p>Taille initiale du cache de réponse principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Dossier racine du cache [/usr/local/scene7/ImageServing/cache] :</span> </p> </td> 
   <td colname="col2"> <p>Dossier de cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Identifiant du propriétaire du serveur d’images [racine] :</span> </p> </td> 
   <td colname="col2"> <p>Le compte utilisateur sous lequel les serveurs de diffusion d’images doivent être installés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Identifiant du groupe de serveurs d’images [racine] :</span> </p> </td> 
   <td colname="col2"> <p>Compte de groupe sous lequel les serveurs de diffusion d’images doivent être installés. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Appuyez sur **[!UICONTROL Entrée]** pour accepter la valeur par défaut ou spécifier une autre valeur.

   Assurez-vous que tous les numéros de port spécifiés sont uniques et ne sont pas utilisés dans d’autres cas sur cet hôte.

   >[!IMPORTANT]
   >
   >Si un compte autre que root est spécifié, vous devez vous assurer que les autorisations d’accès à tous les fichiers et dossiers que le serveur d’images doit lire et/ou écrire sont correctement configurées lorsque ces dossiers sont reconfigurés dans les fichiers de configuration.
   >
   >La diffusion d’images est désormais installée sur [!DNL /usr/local/Scene7/ImageServing]. Certains contenus de rendu d’image sont installés sur [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Vers la fin de l’installation, l’assistant d’installation tente de démarrer Image Server. Si aucune clé de licence valide n’est trouvée, le serveur d’images ne peut pas démarrer. S’il existe une licence valide et que le serveur d’images ne démarre toujours pas, consultez les fichiers journaux.

>[!NOTE]
>
>Si la licence est installée après l’installation d’Image Server, celui-ci doit être démarré manuellement avant d’être utilisé.
