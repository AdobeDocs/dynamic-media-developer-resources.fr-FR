---
title: Prise en charge des technologies d’assistance
description: Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur a un rôle `region` et `aria-label` définie par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé à l’aide de la fonction `Container.LABEL` symbole de localisation.

La vue principale a un rôle `application`. Vous trouverez une brève description de la vue principale dans la section `aria-roledescription`, avec la valeur définie par la variable `ROLE_DESCRIPTION` symbole de localisation du composant d’affichage principal correspondant. Des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte de l’indice d’utilisation provient de la variable `USAGE_HINT` symbole de localisation. Si un libellé est défini dans le champ UserData d’une ressource, la variable `aria-label` est défini avec la valeur de ce libellé.

Les composants qui affichent des échantillons ont un rôle `listbox` avec `aria-label` défini sur la valeur de la variable `LABEL` symbole de localisation de ce composant. Les échantillons individuels ont un rôle `option` avec `aria-setsize` et `aria-posinset` pour décrire la position de l’échantillon dans la visionneuse. Si un échantillon est sélectionné, le paramètre `aria-selected` définie sur `true`.
