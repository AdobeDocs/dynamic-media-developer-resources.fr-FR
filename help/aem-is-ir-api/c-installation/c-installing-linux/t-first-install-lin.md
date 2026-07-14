---
title: Première installation
description: Cette procédure explique comment installer la diffusion d’images pour la première fois sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
TQID: 'https://experienceleague.adobe.com/PppWtEjMNn6CPNvnT03PoFjCW2OxbAJjrFYgbPBi7Iw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 0%

---

# Première installation{#installing-for-the-first-time}

Cette procédure explique comment installer la diffusion d’images pour la première fois sous Linux®.

1. Connectez-vous à votre hôte serveur avec les autorisations root.
1. Créez le dossier [!DNL /usr/local/scene7/licenses].

   Si le fichier de clé de licence de diffusion d’images et/ou de rendu d’images (avec [!DNL .sc8] suffixe de fichier) est disponible, copiez-le dans ce dossier. Sinon, procédez à l’installation et installez la clé de licence ultérieurement.
1. Décompressez et décompressez le fichier tar de distribution du service d’images.
1. Dans le dossier [!DNL Setup] , lancez l’assistant d’installation en exécutant [!DNL ./install-is].

   Si aucune clé de licence n’est trouvée, des instructions décrivant comment obtenir un fichier de licence s’affichent. Faites-le à ce stade ou poursuivez l’installation du service d’images et installez la clé de licence ultérieurement.
1. Lorsque le contrat de licence de l’utilisateur final (CLUF) s’affiche, lisez le contrat de licence, puis saisissez `y` pour continuer.

   Le programme d’installation affiche les invites répertoriées dans le tableau suivant.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> port d'écoute principal [8080]:</span> </p> </td>
   <td colname="col2"> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>Port D'Écoute D'Administration <span class="codeph"> [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Port d'écoute de l'administrateur. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Taille maximale du cache HTTP (Mo) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Taille initiale du cache de réponse principal. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p>Dossier racine du cache <span class="codeph"> [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Dossier du cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID du propriétaire du serveur d’images <span class="codeph"> [root]:</span> </p> </td>
   <td colname="col2"> <p>Compte utilisateur sous lequel le serveur de diffusion d’images doit être installé. </p> </td>
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
   >Si un compte autre que root est spécifié, vous devez vous assurer que les autorisations d’accès pour tous les fichiers et dossiers que le serveur d’images doit lire et écrire sont correctement configurées lorsque ces dossiers sont reconfigurés dans les fichiers de configuration.
   >
   >La diffusion d’images est maintenant installée sur [!DNL /usr/local/Scene7/ImageServing]. Certains contenus de rendu d’image sont installés sur [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Vers la fin de l’installation, l’assistant d’installation tente de démarrer le serveur d’images. Si aucune clé de licence valide n’est trouvée, le serveur d’images ne peut pas démarrer. S’il existe une licence valide et que le serveur d’images ne démarre toujours pas, consultez les fichiers journaux.

>[!NOTE]
>
>Si la licence est installée après l’installation de la diffusion d’images, le serveur d’images doit être démarré manuellement avant utilisation.

