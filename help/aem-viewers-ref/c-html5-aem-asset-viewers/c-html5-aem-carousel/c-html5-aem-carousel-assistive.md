---
title: Prise en charge des technologies d’assistance
description: Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
TQID: 'https://experienceleague.adobe.com/GwKu0Nv5i-7DIsa-4JxKiS95NgCpzeoHqb1-LFG8sfg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur comporte un `region` de rôle et `aria-label`’attribut défini par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons comportent la `button` de rôle et le texte descriptif définis avec l’attribut `aria-label`. La valeur de `aria-label`’attribut est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` attribut est défini en conséquence.

Les boutons qui vous permettent de parcourir les diapositives du carrousel comportent des libellés qui se mettent à jour au moment de l’exécution en fonction de la diapositive actuellement sélectionnée. Le modèle du libellé de ces boutons est défini avec `CAROUSELVIEWER_TOOLTIP_GOTO` symbole de localisation.

La vue principale comporte des `application` de rôle. Une brève description de la vue principale est fournie en `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant de vue principale correspondant. Les conseils de navigation pour les utilisateurs d’un clavier sont fournis à l’aide de `aria-describedby`. Le texte du conseil d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’une ressource, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, les régions et les zones cliquables comportent l’`button` de rôle et le texte descriptif définis avec `aria-label` attribut , avec la valeur du libellé de la zone réactive ou de la zone cliquable. Lorsque l’utilisateur met l’accent sur des zones réactives ou des zones cliquables, des indications de navigation pour les utilisateurs d’un clavier sont fournies à l’aide de `aria-describedby`, le texte de l’indication d’utilisation provenant du symbole de localisation `USAGE_HINT`.
