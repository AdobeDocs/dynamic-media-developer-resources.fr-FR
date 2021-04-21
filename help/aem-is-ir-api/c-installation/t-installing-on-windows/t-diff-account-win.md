---
description: Après l’installation, vous devrez configurer des services pour qu’ils s’exécutent sous l’autre compte utilisateur.
solution: Experience Manager
title: Installation sous un compte utilisateur différent de celui de l’administrateur
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Installation sous un autre compte utilisateur que administrator{#installing-under-a-different-user-account-than-administrator}

Après l’installation, vous devrez configurer des services pour qu’ils s’exécutent sous l’autre compte utilisateur.

1. Accédez aux paramètres de la stratégie de sécurité locale de Windows en cliquant sur **[!UICONTROL menu du Début]** > **[!UICONTROL Paramètres]** > **[!UICONTROL Panneau de Contrôle]** > **[!UICONTROL Outils d&#39;administration]** > **[!UICONTROL Stratégie de sécurité locale]**.
1. Sélectionnez **[!UICONTROL Paramètres de sécurité]** > **[!UICONTROL Stratégies locales]** > **[!UICONTROL Attribution des droits utilisateur]**.
1. Doublon cliquez sur la stratégie &quot;Connexion en tant que service&quot;.
1. Cliquez sur **[!UICONTROL Ajouter..]** et sélectionnez l&#39;utilisateur ou le groupe, puis cliquez sur **[!UICONTROL Ok]** pour confirmer.
