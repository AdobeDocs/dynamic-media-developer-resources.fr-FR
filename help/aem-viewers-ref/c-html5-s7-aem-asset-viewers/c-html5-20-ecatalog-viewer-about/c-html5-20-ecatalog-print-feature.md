---
title: Fonction d’impression
description: La visionneuse vous permet de générer le contenu du catalogue vers une imprimante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Fonction d’impression{#print-feature}

La visionneuse vous permet de générer le contenu du catalogue vers une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. En cliquant sur le bouton, l’utilisateur choisit une plage d’impression et le nombre de pages par feuille.

La qualité de l’impression peut être ajustée à l’aide du `printquality` paramètre de configuration. La définition `printquality` de valeurs supérieures à la valeur par défaut n’est pas recommandée. La raison en est que cela conduit à une consommation de mémoire élevée par le navigateur Web sur le système du client. Assurez-vous également que la taille de réponse d’image maximale définie pour votre société Dynamic Media Classic est supérieure à la valeur configurée `printquality` .

>[!NOTE]
>
>La fonctionnalité Imprimer n’est disponible que sur les systèmes de bureau, à l’exception d’Internet Explorer 9.
