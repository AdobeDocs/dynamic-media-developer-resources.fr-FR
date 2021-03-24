---
description: Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Assistance technique
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel, Accessibilité
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a les attributs de rôle `region` et `aria-label` définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons ont le rôle `button` et un texte descriptif défini avec l&#39;attribut `aria-label`. La valeur de l’attribut `aria-label` est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, l’attribut `aria-disabled` est défini en conséquence.

Les boutons qui vous permettent de naviguer dans les diapositives de carrousel ont des libellés qui se mettent à jour au moment de l&#39;exécution en fonction de la diapositive actuellement sélectionnée. Le modèle d’étiquette de ce bouton est défini avec le symbole de localisation `CAROUSELVIEWER_TOOLTIP_GOTO`.

La vue principale a le rôle `application`. Une brève description de la vue principale est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant principal de vue correspondant. Les conseils de navigation des utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte du conseil d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’un fichier, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, les régions et les zones cliquables ont le rôle `button` et un texte descriptif défini avec l’attribut `aria-label`, avec la valeur de la zone réactive ou du libellé de zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte du conseil d’utilisation provenant du symbole de localisation `USAGE_HINT`.
