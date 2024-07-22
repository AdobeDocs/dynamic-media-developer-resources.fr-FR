---
description: Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Prise en charge des technologies d’assistance
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur a un rôle `region` et un attribut `aria-label` défini par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons ont le rôle `button` et un texte descriptif avec l’attribut `aria-label`. La valeur de l’attribut `aria-label` est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, l’attribut `aria-disabled` est défini en conséquence.

La vue principale a le rôle `application`. Une brève description de la vue principale est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant de vue principal correspondant. Les conseils de navigation pour les utilisateurs de clavier sont fournis à l’aide de `aria-describedby`, le texte de l’indice d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’une ressource, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, régions et zones cliquables ont le rôle `button` et un jeu de texte descriptif avec l’attribut `aria-label`, avec la valeur de la zone réactive ou de l’étiquette de zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation pour les utilisateurs de clavier sont fournis à l’aide de `aria-describedby`, le texte de l’indicateur d’utilisation provenant du symbole de localisation `USAGE_HINT`.

Les miniatures ont le rôle `dialog` avec l’attribut `aria-label` contrôlé par le symbole de localisation `ThumbnailGridView.LABEL`. Les miniatures individuelles ont un rôle `button`. Si une miniature est sélectionnée, l’attribut `aria-selected` est défini sur `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` avec l’attribut `aria-label` défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les échantillons individuels ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position des échantillons dans l’ensemble. Si un échantillon est sélectionné, l’attribut `aria-selected` est défini sur `true`.

Les listes déroulantes sont activées par des boutons avec un attribut `aria-haspopup` supplémentaire défini sur `true` et l’attribut `aria-controls` référençant l’élément de panneau déroulant réel. Le panneau déroulant lui-même a le rôle `menu` avec des sous-éléments ayant le rôle `menuitem`. L’attribut `aria-label` est spécifié pour chaque élément de menu.

L’interface utilisateur de recherche est regroupée dans l’élément avec le rôle `search`. Le champ d’entrée de recherche a le rôle `searchbox` et référence le libellé informatif contrôlé par le symbole de localisation `SearchPanel.INFO_PROMPT` avec l’attribut `aria-describedby` .

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby` .
