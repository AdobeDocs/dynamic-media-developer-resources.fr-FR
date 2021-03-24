---
description: Procédez comme suit pour installer Image Serving pour la première fois sous Windows.
solution: Experience Manager
title: Première installation
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# Première installation de {#installing-for-the-first-time}

Procédez comme suit pour installer Image Serving pour la première fois sous Windows.

1. Connectez-vous à l’hôte du serveur avec des privilèges d’administration.
1. Si vous avez déjà reçu une licence, copiez-la sur votre serveur, puis exécutez l’installation de la licence en cliquant sur le doublon sur le fichier.

   Si vous n’avez pas encore de licence, vous pouvez procéder à l’installation et installer la licence ultérieurement.
1. Extrayez le contenu du fichier compressé de distribution Image Serving.
1. Exécutez [!DNL setup]/ [!DNL setup.exe] pour lancer l’assistant d’installation.
1. Cliquez sur &quot;Suivant&quot; pour passer au contrat de licence de l’utilisateur final (CLUF), lire le contrat de licence, puis cliquez sur **[!UICONTROL Oui]**.

   La boîte de dialogue [!DNL Authentication] s&#39;affiche ensuite.
1. Si une licence est déjà installée et que les informations de licence s&#39;affichent dans la boîte de dialogue [!DNL Authentication], cliquez sur **[!UICONTROL Suivant]** pour continuer.

   Si vous n’avez pas de licence, cliquez sur **[!UICONTROL Demander une licence]**. La boîte de dialogue suivante affiche l&#39;une des adresses MAC de carte d&#39;interface réseau de votre ordinateur. Envoyez ce courrier électronique à cette adresse MAC, au nom de votre société et au produit que vous installez, selon les instructions de l’invite.

   **Important :** La licence est basée sur l’adresse MAC de l’une des cartes d’interface réseau installées sur cet hôte. Si vous désactivez, supprimez ou remplacez cette carte, la licence ne sera plus reconnue comme valide. Veillez à obtenir une licence pour la configuration matérielle que vous utiliserez pour IS.

   Vous pouvez continuer à installer IS sans licence valide et installer la licence ultérieurement. Pour continuer, cliquez sur **[!UICONTROL Précédent]** pour revenir à la boîte de dialogue [!DNL Authentication], puis cliquez sur **[!UICONTROL Suivant]**.
1. Accédez à la page &quot;Paramètres d’administration du serveur de plateformes&quot;. Entrez de nouvelles valeurs ou acceptez les valeurs par défaut.

   Vous pouvez configurer les éléments suivants :

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Port de connexion HTTP du serveur de plateformes </p> </td> 
   <td> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Port d’écoute Admin </p> </td> 
   <td> <p>Port d’écoute Admin </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Taille du cache du serveur de plateformes en Mo </p> </td> 
   <td> <p>Taille initiale du cache de réponse principal </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Emplacement du cache du serveur de plateformes </p> </td> 
   <td> <p>Dossier cache PS </p> </td> 
  </tr> 
 </tbody> 
</table>

Les numéros de port spécifiés doivent être uniques et ne pas être utilisés par d&#39;autres applications ou services.

L’écran suivant permet de vérifier les paramètres sélectionnés.
1. Cliquez sur **[!UICONTROL Précédent]** pour apporter des modifications ou sur **[!UICONTROL Suivant]** pour début l’installation.
1. Cliquez sur **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.
