---
title: Prise en charge des technologies d’assistance
description: Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets,Accessibility
role: Developer,User
exl-id: 6cf7f739-cbfb-4fac-8632-904a0d40ad05
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur a un rôle `region` et `aria-label` définie par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé à l’aide de la fonction `Container.LABEL` symbole de localisation.

Les boutons ont un rôle `button` et texte descriptif avec `aria-label` attribut. La valeur de `aria-label` est renseigné à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` est défini en conséquence.

La vue principale a un rôle `application`. Vous trouverez une brève description de la vue principale dans la section `aria-roledescription`, avec la valeur définie par la variable `ROLE_DESCRIPTION` symbole de localisation du composant d’affichage principal correspondant. Des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte de l’indice d’utilisation provient de la variable `USAGE_HINT` symbole de localisation. Si un libellé est défini dans le champ UserData d’une ressource, la variable `aria-label` est défini avec la valeur de ce libellé.

Les composants qui affichent des échantillons ont un rôle `listbox` avec `aria-label` défini sur la valeur de la variable `LABEL` symbole de localisation de ce composant. Les échantillons individuels ont un rôle `option` avec `aria-setsize` et `aria-posinset` pour décrire la position de l’échantillon dans la visionneuse. Si un échantillon est sélectionné, le paramètre `aria-selected` définie sur `true`.

Les composants de curseur ont un rôle `slider` avec des attributs `aria-valuenow`, `aria-valuemin`, et `aria-valuemax` pour décrire la position actuelle du curseur.
