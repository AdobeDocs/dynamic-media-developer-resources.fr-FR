---
title: Soutien aux technologies d’assistance
description: Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Soutien aux technologies d’assistance{#assistive-technology-support}

Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

Le rôle `region` et `aria-label` l’attribut de l’élément visionneuse de niveau supérieur sont définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler l’étiquette avec le symbole de `Container.LABEL` localisation.

La vue principale a un rôle `application`. Une brève description de la vue principale est fournie dans `aria-roledescription`, avec la valeur définie par le `ROLE_DESCRIPTION` symbole de localisation du composant Vue principale correspondant. Les conseils de navigation pour les utilisateurs de clavier sont fournis à l’aide `aria-describedby`de , le texte de l’indice d’utilisation provient du symbole de `USAGE_HINT` localisation. Si une étiquette est définie dans le champ UserData, l’attribut `aria-label` est défini avec la valeur de cette étiquette.

Les zones réactives, les régions et les zones cliquables ont le rôle `button` et le texte descriptif définis avec `aria-label` l’attribut, avec la valeur du point réactif ou de l’étiquette de zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide `aria-describedby`de , le texte de l’indicateur d’utilisation provenant du symbole de `USAGE_HINT` localisation.
