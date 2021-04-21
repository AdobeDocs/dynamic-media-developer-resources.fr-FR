---
description: Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.
solution: Experience Manager
title: Données utilisateur
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---


# Données utilisateur{#userdata}

Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.

## Propriétés {#section-06f2002b77d54a64be07f12fff54ad13}

Valeur de chaîne de texte. Il est recommandé d’utiliser la mise en forme [data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) des propriétés. Si le formatage des données de propriété n&#39;est pas utilisé, la chaîne de texte ne doit pas contenir le caractère &quot;=&quot;.

Les clients du lecteur de zoom, de rotation et de brochure supposent que ce champ utilise le formatage des données de propriété. Ces clients utilisent ce champ pour la configuration et la personnalisation de la visionneuse. Consultez la documentation du lecteur pour plus de détails.

Ce champ participe à la localisation des chaînes de texte. Pour plus d&#39;informations, consultez la [Localisation de chaînes de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans le *Guide de référence du protocole HTTP*.

## Par défaut {#section-7ee879762130467199745f2abc662f1e}

Aucune

## Voir aussi {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , Localisation de chaînes de  [texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
