---
title: Installation sous un compte utilisateur différent de celui de l’administrateur
description: Après l’installation, configurez les services à exécuter sous l’autre compte utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 20bb00cb-3af6-4573-bbff-8c4f984ed2ae
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Installation sous un compte utilisateur différent de celui de l’administrateur{#installing-under-a-different-user-account-than-administrator}

Après l’installation, configurez les services à exécuter sous l’autre compte utilisateur.

1. Accédez aux paramètres de la stratégie de sécurité locale de Windows en sélectionnant **[!UICONTROL Menu Démarrer]** > **[!UICONTROL Paramètres]** > **[!UICONTROL Panneau de Contrôle]** > **[!UICONTROL Outils d’administration]** > **[!UICONTROL Stratégie de sécurité locale]**.
1. Sélectionnez **[!UICONTROL Paramètres de sécurité]** > **[!UICONTROL Stratégies locales]** > **[!UICONTROL Attribution des droits utilisateur]**.
1. Double-cliquez sur la stratégie **[!UICONTROL Log on as a service]**.
1. Sélectionnez **[!UICONTROL Ajouter...]** et sélectionnez l’utilisateur ou le groupe, puis **[!UICONTROL Ok]** pour confirmer.
