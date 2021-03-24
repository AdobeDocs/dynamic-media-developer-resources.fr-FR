---
description: Le lecteur de contenu vous permet de générer le contenu du catalogue sur une imprimante.
solution: Experience Manager
title: Fonction d’impression
feature: Dynamic Media Classic, Visionneuses, SDK/API, Recherche de catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Fonction d&#39;impression{#print-feature}

Le lecteur de contenu vous permet de générer le contenu du catalogue sur une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. En cliquant sur le bouton, l’utilisateur peut choisir une plage d’impression et le nombre de pages par feuille.

La qualité de l&#39;impression peut être ajustée à l&#39;aide du paramètre de configuration `printquality`. Notez que la définition de `printquality` sur des valeurs significativement plus élevées que la valeur par défaut n’est pas recommandée. La raison en est qu&#39;elle conduit à une très forte consommation de mémoire par le navigateur Web sur le système du client. Assurez-vous également que la taille maximale de réponse d’image définie pour votre société Dynamic Media Classic est supérieure à la valeur `printquality` configurée.

>[!NOTE]
>
>La fonction Imprimer est disponible uniquement sur les systèmes de bureau, à l’exception d’Internet Explorer 9.

