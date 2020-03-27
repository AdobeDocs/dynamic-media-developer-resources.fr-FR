---
description: Procédez comme suit pour installer Image Serving pour la première fois sous Windows.
seo-description: Procédez comme suit pour installer Image Serving pour la première fois sous Windows.
seo-title: Première installation
solution: Experience Manager
title: Première installation
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Première installation{#installing-for-the-first-time}

Procédez comme suit pour installer Image Serving pour la première fois sous Windows.

1. Connectez-vous à l’hôte du serveur avec des privilèges d’administrateur.
1. Si vous avez déjà reçu une licence, copiez-la sur votre serveur, puis exécutez l’installation de la licence en cliquant  sur le fichier.

   Si vous n’avez pas encore de licence, vous pourrez procéder à l’installation et installer la licence ultérieurement.
1. Extrayez le contenu du fichier .zip de distribution Image Serving.
1. Exécutez [!DNL setup]/ [!DNL setup.exe] pour lancer l’assistant d’installation.
1. Cliquez sur &quot;Suivant&quot; pour accéder au contrat de licence de l’utilisateur final (CLUF), lisez le contrat de licence, puis cliquez sur **[!UICONTROL Oui]**.

   La [!DNL Authentication] boîte de dialogue suivante s’affiche.
1. Si une licence est déjà installée et que les informations de licence s’affichent dans la boîte de [!DNL Authentication] dialogue, cliquez sur **[!UICONTROL Suivant]** pour continuer.

   Si vous n’avez pas de licence, cliquez sur **[!UICONTROL Demander une licence]**. La boîte de dialogue suivante affiche l’une des adresses MAC de la carte d’interface réseau de votre ordinateur. Envoyez par courrier électronique cette adresse MAC, le nom de votre  et le produit que vous installez, selon les instructions de l’invite.

   **Important :** La licence est basée sur l&#39;adresse MAC de l&#39;une des cartes d&#39;interface réseau installées sur cet hôte. Si vous désactivez, supprimez ou remplacez cette carte, la licence ne sera plus reconnue comme valide. Veillez à obtenir une licence pour la configuration matérielle que vous utiliserez pour IS.

   Vous pouvez continuer à installer IS sans licence valide et installer la licence ultérieurement. Pour continuer, cliquez sur **[!UICONTROL Précédent]** pour revenir à la [!DNL Authentication] boîte de dialogue, puis cliquez sur **[!UICONTROL Suivant]**.
1. Accédez à la page &quot;Paramètres d’administration du serveur de plateformes&quot;. Entrez de nouvelles valeurs ou acceptez les valeurs par défaut.

   Vous pouvez configurer les éléments suivants :

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Port de connexion HTTP du serveur de plateformes </p> </td> 
   <td> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Port d’écoute d’administrateur </p> </td> 
   <td> <p>Port d’écoute d’administrateur </p> </td> 
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

L’écran suivant vous donne la possibilité de consulter les paramètres sélectionnés.
1. Cliquez sur **[!UICONTROL Précédent]** pour apporter des modifications ou sur **[!UICONTROL Suivant]** pour de l’installation.
1. Cliquez sur **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.
