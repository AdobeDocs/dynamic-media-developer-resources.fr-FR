---
description: Pour installer Image Serving pour la première fois sous Windows, procédez comme suit.
solution: Experience Manager
title: Première installation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Première installation{#installing-for-the-first-time}

Pour installer Image Serving pour la première fois sous Windows, procédez comme suit.

1. Connectez-vous à l’hôte de votre serveur avec les droits d’administrateur.
1. Si vous avez déjà reçu une licence, copiez-la sur votre serveur, puis exécutez l’installation de la licence en double-cliquant sur le fichier.

   Si vous ne disposez pas encore d’une licence, vous pouvez poursuivre l’installation et installer la licence ultérieurement.
1. Extrayez le contenu du fichier zip de distribution Image Serving .
1. Exécutez [!DNL setup]/ [!DNL setup.exe] pour lancer l’assistant d’installation.
1. Cliquez sur &quot;Suivant&quot; pour accéder au contrat de licence de l’utilisateur final (EULA), lisez le contrat de licence, puis cliquez sur **[!UICONTROL Oui]**.

   La boîte de dialogue [!DNL Authentication] s’affiche ensuite.
1. Si une licence est déjà installée et que les informations de licence s’affichent dans la boîte de dialogue [!DNL Authentication], cliquez sur **[!UICONTROL Suivant]** pour continuer.

   Si vous ne disposez pas d’une licence, cliquez sur **[!UICONTROL Demander la licence]**. La boîte de dialogue suivante affiche l’une des adresses MAC de carte d’interface réseau de votre ordinateur. Envoyez par courrier électronique cette adresse MAC, le nom de votre société et le produit que vous installez selon la direction de l’invite.

   **Important :** La licence est basée sur l’adresse MAC de l’une des cartes d’interface réseau installées sur cet hôte. Si vous désactivez, supprimez ou remplacez cette carte, la licence ne sera plus reconnue comme valide. Veillez à obtenir une licence pour la configuration matérielle que vous utiliserez pour IS.

   Vous pouvez continuer à installer IS sans licence valide et installer la licence ultérieurement. Pour continuer, cliquez sur **[!UICONTROL Précédent]** pour revenir à la boîte de dialogue [!DNL Authentication], puis cliquez sur **[!UICONTROL Suivant]**.
1. Accédez à la page &quot;Paramètres d’administration du serveur de plateforme&quot;. Saisissez de nouvelles valeurs si nécessaire ou acceptez les valeurs par défaut.

   Vous pouvez configurer les éléments suivants :

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Port de connexion HTTP du serveur de plateformes </p> </td> 
   <td> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Port d’écoute de l’administrateur </p> </td> 
   <td> <p>Port d’écoute de l’administrateur </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Taille du cache du serveur de plateformes en Mo </p> </td> 
   <td> <p>Taille initiale du cache de réponse principal </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Emplacement du cache du serveur de plateformes </p> </td> 
   <td> <p>Dossier de cache PS </p> </td> 
  </tr> 
 </tbody> 
</table>

Les numéros de port spécifiés doivent être uniques et ne pas être utilisés par d’autres applications ou services.

L’écran suivant permet de consulter les paramètres sélectionnés.
1. Cliquez sur **[!UICONTROL Précédent]** pour apporter des modifications ou sur **[!UICONTROL Suivant]** pour lancer l’installation.
1. Cliquez sur **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.
