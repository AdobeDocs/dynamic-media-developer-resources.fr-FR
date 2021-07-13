---
description: Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.
solution: Experience Manager
title: Données utilisateur
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 8%

---

# Données utilisateur{#userdata}

Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.

## Propriétés {#section-06f2002b77d54a64be07f12fff54ad13}

Valeur de chaîne de texte. Il est recommandé d’utiliser la mise en forme [data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) des propriétés. Si la mise en forme des données de propriété n’est pas utilisée, la chaîne de texte ne doit pas contenir le caractère &quot;=&quot;.

Les clients de la visionneuse de zoom, à 360° et de brochures considèrent que ce champ permet d’utiliser le formatage des données de propriété. Ces clients utilisent ce champ pour la configuration et la personnalisation de la visionneuse. Pour plus d’informations, consultez la documentation du lecteur .

Ce champ participe à la localisation de la chaîne de texte. Pour plus d’informations, reportez-vous à la section [Localisation des chaînes de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans la *Référence du protocole HTTP*.

## Par défaut {#section-7ee879762130467199745f2abc662f1e}

Aucune

## Voir aussi {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [localisation des chaînes de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
