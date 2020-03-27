---
description: Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
seo-description: Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
seo-title: Prise en charge des technologies d'assistance
solution: Experience Manager
title: Prise en charge des technologies d'assistance
topic: Dynamic media
uuid: 52f5dad9-7309-4385-99bc-79d02d3ba2d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge des technologies d&#39;assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a un rôle `region` `aria-label` et un attribut définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler l’étiquette à l’aide du `Container.LABEL` symbole .

Les boutons ont le rôle `button` et le texte descriptif défini avec `aria-label` attribut. La valeur de `aria-label` l’attribut est renseignée à partir de la valeur du symbole de  du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` l’attribut est défini en conséquence.

Les composants du curseur ont le rôle `slider` avec des attributs `aria-valuenow`, `aria-valuemin`et `aria-valuemax` pour décrire la position actuelle du curseur.

Les  déroulantes sont activées par des boutons avec des `aria-haspopup` attributs supplémentaires définis pour `true` et `aria-controls` des attributs référençant l’élément de panneau déroulant réel. Le panneau déroulant lui-même a le rôle `menu` avec des sous-éléments ayant le rôle `menuitem`. L&#39; `aria-label` attribut spécifié est affecté à chaque élément de menu.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’ `aria-labelledby` attribut.
