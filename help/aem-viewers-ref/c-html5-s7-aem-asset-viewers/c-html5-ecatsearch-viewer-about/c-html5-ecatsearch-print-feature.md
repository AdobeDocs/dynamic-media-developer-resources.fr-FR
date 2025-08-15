---
description: La visionneuse vous permet de générer le contenu du catalogue vers une imprimante.
solution: Experience Manager
title: Fonction d’impression
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Fonction d’impression{#print-feature}

La visionneuse vous permet de générer le contenu du catalogue vers une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. En cliquant sur le bouton, l’utilisateur choisit une plage d’impression et le nombre de pages par feuille.

La qualité de l’impression peut être ajustée à l’aide du `printquality` paramètre de configuration. Notez que la définition `printquality` de valeurs nettement supérieures à la valeur par défaut n’est pas recommandée. La raison en est que cela conduit à une consommation de mémoire très élevée par le navigateur Web sur le système du client. Assurez-vous également que la taille de réponse d’image maximale définie pour votre société Dynamic Media Classic est supérieure à la valeur configurée `printquality` .

>[!NOTE]
>
>La fonctionnalité Imprimer n’est disponible que sur les systèmes de bureau, à l’exception d’Internet Explorer 9.
