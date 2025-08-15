---
title: Première installation
description: Suivez ces étapes pour installer Image Serving pour la première fois sous Windows.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Première installation{#installing-for-the-first-time}

Suivez ces étapes pour installer Image Serving pour la première fois sous Windows.

1. Connectez-vous à votre hôte de serveur avec des droits d’administrateur.
1. Si vous avez déjà reçu une licence, copiez-la sur votre serveur, puis exécutez l’installation de la licence en double-cliquant sur le fichier.

   Si vous n’avez pas encore de licence, vous pouvez procéder à l’installation et installer la licence ultérieurement.

1. Extract le contenu du fichier compressé de distribution Image Server.
1. Launch l’assistant d’installation, en exécutant [!DNL setup]/ [!DNL setup.exe].
1. Sélectionnez **[!UICONTROL Suivant]** pour accéder au Contrat de licence utilisateur final (CLUF), lisez le contrat de licence, puis sélectionnez **[!UICONTROL Oui]**.

   La [!DNL Authentication] boîte de dialogue s’affiche ensuite.
1. Si une licence est déjà installée et que les informations de licence apparaissent dans la boîte de [!DNL Authentication] dialogue, sélectionnez **[!UICONTROL Suivant]** pour continuer.

   Si vous n’avez pas de licence, sélectionnez **[!UICONTROL Demander une licence]**. La boîte de dialogue suivante affiche l’une des adresses MAC de la carte d’interface réseau de votre machine. Envoyez par e-mail cette adresse MAC, le nom de votre société et le produit que vous installez comme indiqué par l’invite.

   **Important :** La licence est basée sur l’adresse MAC de l’une des cartes d’interface réseau installées sur cet hôte. Si vous désactivez, supprimez ou remplacez cette carte, la licence n’est plus reconnue comme valide. Veillez à obtenir une licence pour la configuration matérielle que vous utilisez pour Image Server.

   Vous pouvez continuer à installer IS sans licence valide et installer la licence ultérieurement. Pour continuer, sélectionnez **[!UICONTROL Retour]** pour revenir à la [!DNL Authentication] boîte de dialogue, puis sélectionnez **[!UICONTROL Suivant]**.
1. Passez à la page &quot;[!DNL Platform Server] Paramètres d’administration « . Entrez de nouvelles valeurs si nécessaire ou acceptez les valeurs par défaut.

   Vous pouvez configurer les éléments suivants :

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Port de connexion HTTP </p> </td>
      <td> <p>Port d’écoute HTTP principal pour Image Serving et Image Rendering </p> </td>
   </tr> 
   <tr> 
      <td> <p> Port d’écoute Admin </p> </td>
      <td> <p>Port d’écoute Admin </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] Taille du cache en Mo </p> </td>
      <td> <p>Taille initiale du cache de réponse principal </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] Emplacement du cache </p> </td>
      <td> <p>Dossier de cache PS </p> </td>
   </tr>
   </tbody>
   </table>

   Les numéros de port spécifiés doivent être uniques et ne pas être utilisés par d’autres applications ou services.

   L’écran suivant vous permet de vérifier les paramètres sélectionnés.

1. Sélectionnez **[!UICONTROL Précédent]** pour effectuer des modifications ou Suivant **** pour démarrer l’installation.

1. Sélectionnez **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.
