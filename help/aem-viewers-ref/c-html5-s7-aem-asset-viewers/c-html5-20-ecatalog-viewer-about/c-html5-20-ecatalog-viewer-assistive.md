---
title: Prise en charge des technologies d’assistance
description: Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur a un rôle `region` et `aria-label` définie par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé à l’aide de la fonction `Container.LABEL` symbole de localisation.

Les boutons ont un rôle `button` et texte descriptif avec le `aria-label` attribut. La valeur de `aria-label` est renseigné à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, la variable `aria-disabled` est défini en conséquence.

La vue principale a un rôle `application`. Vous trouverez une brève description de la vue principale dans la section `aria-roledescription`, avec la valeur définie par la variable `ROLE_DESCRIPTION` symbole de localisation du composant d’affichage principal correspondant. Des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte de l’indice d’utilisation provient de la variable `USAGE_HINT` symbole de localisation. Si un libellé est défini dans le champ UserData d’une ressource, la variable `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, régions et zones cliquables ont un rôle `button` et texte descriptif avec `aria-label` avec la valeur de la zone réactive ou du libellé de la zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation sont fournis à l’aide du `aria-describedby`, avec le texte de l’indicateur d’utilisation provenant de la fonction `USAGE_HINT` symbole de localisation.

Les miniatures ont un rôle `dialog` avec `aria-label` contrôlé par l’attribut `ThumbnailGridView.LABEL` symbole de localisation. Les miniatures individuelles ont un rôle `button`. Si une miniature est sélectionnée, elle est récupérée. `aria-selected` définie sur `true`.

Les composants qui affichent des échantillons ont un rôle `listbox` avec `aria-label` défini sur la valeur de la variable `LABEL` symbole de localisation de ce composant. Les échantillons individuels ont un rôle `option` avec `aria-setsize` et `aria-posinset` pour décrire la position de l’échantillon dans la visionneuse. Si un échantillon est sélectionné, le paramètre `aria-selected` définie sur `true`.

Les listes déroulantes sont activées par des boutons avec des `aria-haspopup` définie sur `true` et le `aria-controls` faisant référence à l’élément de panneau déroulant réel. Le panneau déroulant lui-même a le rôle `menu` avec des sous-éléments ayant un rôle `menuitem`. Chaque élément de menu comporte la variable `aria-label` spécifié.

Les boîtes de dialogue modales ont un rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par le `aria-labelledby` attribut.
