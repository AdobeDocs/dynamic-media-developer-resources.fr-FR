---
title: Première installation
description: Pour installer Image Serving pour la première fois sous Windows, procédez comme suit.
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

Pour installer Image Serving pour la première fois sous Windows, procédez comme suit.

1. Connectez-vous à l’hôte de votre serveur avec les droits d’administrateur.
1. Si vous avez déjà reçu une licence, copiez-la sur votre serveur, puis exécutez l’installation de la licence en double-cliquant sur le fichier.

   Si vous ne disposez pas encore d’une licence, vous pouvez poursuivre l’installation et installer la licence ultérieurement.

1. Extrayez le contenu du fichier zip de distribution Image Serving .
1. Lancez l’assistant d’installation en exécutant [!DNL setup]/ [!DNL setup.exe].
1. Sélectionner **[!UICONTROL Suivant]** pour accéder au contrat de licence de l’utilisateur final (EULA), lisez le contrat de licence, puis sélectionnez **[!UICONTROL Oui]**.

   Le [!DNL Authentication] s’affiche ensuite.
1. Si une licence est déjà installée, les informations de licence apparaissent dans la variable [!DNL Authentication] boîte de dialogue, sélectionnez **[!UICONTROL Suivant]** pour continuer.

   Si vous ne disposez pas d’une licence, sélectionnez **[!UICONTROL Demande de licence]**. La boîte de dialogue suivante affiche l’une des adresses MAC de carte d’interface réseau de votre ordinateur. Envoyez par courrier électronique cette adresse MAC, le nom de votre société et le produit que vous installez selon la direction de l’invite.

   **Important :** La licence est basée sur l’adresse MAC de l’une des cartes d’interface réseau installées sur cet hôte. Si vous désactivez, supprimez ou remplacez cette carte, la licence n’est plus reconnue comme valide. Veillez à obtenir une licence pour la configuration matérielle que vous utilisez pour la diffusion d’images.

   Vous pouvez continuer à installer IS sans licence valide et installer la licence ultérieurement. Pour continuer, sélectionnez **[!UICONTROL Précédent]** pour revenir au [!DNL Authentication] , puis sélectionnez **[!UICONTROL Suivant]**.
1. Accédez au[!DNL Platform Server] Paramètres d’administration&quot;. Saisissez de nouvelles valeurs si nécessaire ou acceptez les valeurs par défaut.

   Vous pouvez configurer les éléments suivants :

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Port de connexion HTTP </p> </td>
      <td> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images </p> </td>
   </tr> 
   <tr> 
      <td> <p> Port d’écoute de l’administrateur </p> </td>
      <td> <p>Port d’écoute de l’administrateur </p> </td>
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

   L’écran suivant permet de consulter les paramètres sélectionnés.

1. Sélectionner **[!UICONTROL Précédent]** pour apporter des modifications, ou sélectionnez **[!UICONTROL Suivant]** pour lancer l’installation.

1. Sélectionner **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.
