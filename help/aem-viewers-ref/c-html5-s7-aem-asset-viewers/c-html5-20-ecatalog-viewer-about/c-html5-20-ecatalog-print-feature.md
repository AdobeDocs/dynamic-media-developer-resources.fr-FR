---
title: Fonction d’impression
description: La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.
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

La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. Cliquer sur le bouton permet à l&#39;utilisateur de choisir une plage d&#39;impression et le nombre de pages par feuille.

La qualité de l&#39;impression peut être ajustée à l&#39;aide du paramètre de configuration `printquality`. Il n&#39;est pas recommandé de définir `printquality` sur des valeurs supérieures à la valeur par défaut. Cela est dû au fait que le navigateur Web consomme beaucoup de mémoire sur le système du client. Assurez-vous également que la taille maximale de réponse de l’image définie pour votre société Dynamic Media Classic est supérieure à la valeur `printquality` configurée.

>[!NOTE]
>
>La fonction d’impression n’est disponible que sur les ordinateurs de bureau, à l’exception d’Internet Explorer 9.
