---
title: Première installation
description: Procédez comme suit pour installer la diffusion d’images pour la première fois sous Windows.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
TQID: 'https://experienceleague.adobe.com/bL2S5Uv6RkMg5CbPb6mXZvDPf30sHkuXPKc6m7TNXqc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 0%

---

# Première installation{#installing-for-the-first-time}

Procédez comme suit pour installer la diffusion d’images pour la première fois sous Windows.

1. Connectez-vous à votre hôte de serveur avec des droits d’administrateur.
1. Si vous avez déjà reçu une licence, copiez-la sur votre serveur, puis exécutez l&#39;installation de la licence en double-cliquant sur le fichier.

   Si vous ne possédez pas encore de licence, vous pouvez procéder à l’installation et installer la licence ultérieurement.

1. Extrayez le contenu du fichier zip de distribution du service d’images.
1. Lancez l&#39;assistant d&#39;installation en exécutant [!DNL setup]/ [!DNL setup.exe].
1. Sélectionnez **[!UICONTROL Suivant]** pour accéder au contrat de licence de l’utilisateur final (CLUF), lisez le contrat de licence, puis sélectionnez **[!UICONTROL Oui]**.

   La boîte de dialogue [!DNL Authentication] s’affiche ensuite.
1. Si une licence est déjà installée et que les informations de licence apparaissent dans la boîte de dialogue [!DNL Authentication], sélectionnez **[!UICONTROL Suivant]** pour continuer.

   Si vous ne possédez pas de licence, sélectionnez **[!UICONTROL Demander une licence]**. La boîte de dialogue suivante affiche l&#39;une des adresses MAC de carte d&#39;interface réseau de votre ordinateur. Envoyez cette adresse MAC, le nom de votre société et le produit que vous installez conformément aux instructions de l’invite.

   **Important :** la licence est basée sur l&#39;adresse MAC de l&#39;une des cartes d&#39;interface réseau installées sur cet hôte. Si vous désactivez, supprimez ou remplacez cette carte, la licence n&#39;est plus reconnue comme valide. Veillez à obtenir une licence pour la configuration matérielle que vous utilisez pour la diffusion d’images.

   Vous pouvez continuer à installer IS sans licence valide et installer la licence ultérieurement. Pour continuer, sélectionnez **[!UICONTROL Précédent]** pour revenir à la boîte de dialogue [!DNL Authentication], puis sélectionnez **[!UICONTROL Suivant]**.
1. Accédez à la page « Paramètres d’administration [!DNL Platform Server] ». Saisissez les nouvelles valeurs selon vos besoins ou acceptez les valeurs par défaut.

   Vous pouvez configurer les éléments suivants :

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> Port de connexion HTTP [!DNL Platform Server] </p> </td>
      <td> <p>Port d’écoute HTTP principal pour la diffusion d’images et le rendu d’images </p> </td>
   </tr> 
   <tr> 
      <td> <p> Port d'écoute de l'administrateur </p> </td>
      <td> <p>Port d'écoute de l'administrateur </p> </td>
   </tr> 
   <tr> 
      <td> <p> Taille de cache [!DNL Platform Server] en Mo </p> </td>
      <td> <p>Taille initiale du cache de réponse principal </p> </td>
   </tr>
   <tr> 
      <td> <p> Emplacement du cache [!DNL Platform Server] </p> </td>
      <td> <p>Dossier du cache PS </p> </td>
   </tr>
   </tbody>
   </table>

   Les numéros de port spécifiés doivent être uniques et non utilisés par d&#39;autres applications ou services.

   L’écran suivant permet de passer en revue les paramètres sélectionnés.

1. Sélectionnez **[!UICONTROL Précédent]** pour apporter des modifications, ou sélectionnez **[!UICONTROL Suivant]** pour démarrer l’installation.

1. Sélectionnez **[!UICONTROL Terminer]** pour quitter l’assistant d’installation.
