---
description: Après l’installation, vous devrez configurer des services pour qu’ils s’exécutent sous l’autre compte utilisateur.
seo-description: Après l’installation, vous devrez configurer des services pour qu’ils s’exécutent sous l’autre compte utilisateur.
seo-title: Installation sous un compte utilisateur différent de celui de l’administrateur
solution: Experience Manager
title: Installation sous un compte utilisateur différent de celui de l’administrateur
topic: Scene7 Image Serving - Image Rendering API
uuid: c5944515-c378-45c3-bc18-3261133ba009
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Installation sous un autre compte utilisateur que administrator{#installing-under-a-different-user-account-than-administrator}

Après l’installation, vous devrez configurer des services pour qu’ils s’exécutent sous l’autre compte utilisateur.

1. Accédez aux paramètres de la stratégie de sécurité locale de Windows en cliquant sur **[!UICONTROL menu du Début]** > **[!UICONTROL Paramètres]** > **[!UICONTROL Panneau de Contrôle]** > **[!UICONTROL Outils d&#39;administration]** > **[!UICONTROL Stratégie de sécurité locale]**.
1. Sélectionnez **[!UICONTROL Paramètres de sécurité]** > **[!UICONTROL Stratégies locales]** > **[!UICONTROL Attribution des droits utilisateur]**.
1. Doublon cliquez sur la stratégie &quot;Connexion en tant que service&quot;.
1. Cliquez sur **[!UICONTROL Ajouter..]** et sélectionnez l&#39;utilisateur ou le groupe, puis cliquez sur **[!UICONTROL Ok]** pour confirmer.
