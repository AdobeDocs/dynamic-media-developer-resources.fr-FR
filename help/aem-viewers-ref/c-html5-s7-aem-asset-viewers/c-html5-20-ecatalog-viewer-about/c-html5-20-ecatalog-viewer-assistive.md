---
description: Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Prise en charge des technologies d’assistance
feature: Dynamic Media Classic,Visionneuses,SDK/API,eCatalog,Accessibilité
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur a un rôle `region` et un attribut `aria-label` défini par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons ont le rôle `button` et un texte descriptif défini avec l’attribut `aria-label` . La valeur de l’attribut `aria-label` est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, l’attribut `aria-disabled` est défini en conséquence.

La vue principale a le rôle `application`. Une brève description de la vue principale est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant de vue principal correspondant. Les conseils de navigation pour les utilisateurs de clavier sont fournis à l’aide de `aria-describedby`, le texte de l’indice d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’une ressource, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, régions et zones cliquables ont le rôle `button` et un texte descriptif défini avec l’attribut `aria-label`, avec la valeur de la zone réactive ou de l’étiquette de zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation sont fournis pour les utilisateurs du clavier à l’aide de `aria-describedby`, le texte de l’indicateur d’utilisation provenant du symbole de localisation `USAGE_HINT`.

Les miniatures ont le rôle `dialog` avec l’attribut `aria-label` contrôlé par le symbole de localisation `ThumbnailGridView.LABEL`. Les miniatures individuelles ont un rôle `button`. Si une miniature est sélectionnée, l’attribut `aria-selected` est défini sur `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` avec l’attribut `aria-label` défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les échantillons individuels ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position de l’échantillon dans l’ensemble. Si un échantillon est sélectionné, l’attribut `aria-selected` est défini sur `true`.

Les listes déroulantes sont activées par des boutons avec un attribut `aria-haspopup` supplémentaire défini sur `true` et l&#39;attribut `aria-controls` référençant l&#39;élément réel du panneau déroulant. Le panneau déroulant lui-même a le rôle `menu` avec des sous-éléments ayant le rôle `menuitem`. L’attribut `aria-label` est spécifié pour chaque élément de menu.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby` .
