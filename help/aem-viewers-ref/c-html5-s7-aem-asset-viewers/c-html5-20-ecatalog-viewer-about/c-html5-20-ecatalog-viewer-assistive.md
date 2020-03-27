---
description: Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
seo-description: Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
seo-title: Prise en charge des technologies d'assistance
solution: Experience Manager
title: Prise en charge des technologies d'assistance
topic: Dynamic media
uuid: 8565383e-5c13-4af0-9b6e-2d583c18f19c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge des technologies d&#39;assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a un rôle `region` `aria-label` et un attribut définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler l’étiquette à l’aide du `Container.LABEL` symbole .

Les boutons ont le rôle `button` et le texte descriptif défini avec l’ `aria-label` attribut. La valeur de `aria-label` l’attribut est renseignée à partir de la valeur du symbole de  du bouton. Lorsqu’un bouton est désactivé, l’ `aria-disabled` attribut est défini en conséquence.

Le principal a un rôle `application`. Une brève description de la  principale du est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de la  de du composant `ROLE_DESCRIPTION` principal de l&#39;ensemble de l&#39;ensemble. Les conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide `aria-describedby`, le texte du conseil d’utilisation provient du symbole `USAGE_HINT` . Si un libellé est défini dans le champ UserData d’un fichier, l’ `aria-label` attribut est défini avec la valeur de ce libellé.

Les zones réactives, les régions et les zones cliquables ont le rôle `button` et le texte descriptif défini avec `aria-label` attribut, avec la valeur du libellé de zone réactive ou de zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide `aria-describedby`, le texte du conseil d’utilisation provenant du symbole de l’ `USAGE_HINT` .

Les miniatures ont le rôle `dialog` dont l’attribut est contrôlé par le `aria-label` `ThumbnailGridView.LABEL` symbole  de l’. Les miniatures individuelles ont un rôle `button`. Si une miniature est sélectionnée, l’attribut est défini sur `aria-selected` `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` dont l’attribut `aria-label` est défini sur la valeur du symbole de  de `LABEL` de ce composant. Les nuances individuelles ont le rôle `option` avec `aria-setsize` `aria-posinset` et les attributs pour décrire la position des nuances dans la visionneuse. Si une nuance est sélectionnée, l’ `aria-selected` attribut est défini sur `true`.

Les  déroulantes sont activées par des boutons dont l’ `aria-haspopup` attribut supplémentaire est défini sur `true` et l’attribut `aria-controls` référençant l’élément de panneau déroulant réel. Le panneau déroulant lui-même a le rôle `menu` avec des sous-éléments ayant le rôle `menuitem`. L&#39; `aria-label` attribut spécifié est affecté à chaque élément de menu.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’ `aria-labelledby` attribut.
