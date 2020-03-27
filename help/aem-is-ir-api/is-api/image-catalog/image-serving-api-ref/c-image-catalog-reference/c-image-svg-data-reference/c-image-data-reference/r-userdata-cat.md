---
description: Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.
seo-description: Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.
seo-title: Données utilisateur
solution: Experience Manager
title: Données utilisateur
topic: Scene7 Image Serving - Image Rendering API
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Données utilisateur{#userdata}

Données utilisateur. Le serveur renvoie le contenu de ce champ au client en réponse à req=userdata.

## Propriétés {#section-06f2002b77d54a64be07f12fff54ad13}

Valeur de chaîne de texte. Il est recommandé d’utiliser le formatage des données [de](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) propriété. Si le formatage des données de propriété n’est pas utilisé, la chaîne de texte ne doit pas contenir le caractère &quot;=&quot;.

Les clients du lecteur de zoom, de rotation et de brochure supposent que ce champ utilise le formatage des données de propriété. Ces clients utilisent ce champ pour la configuration et la personnalisation de la visionneuse. Pour plus d’informations, reportez-vous à la documentation du lecteur.

Ce champ participe aux  de chaîne de texte. Pour plus d’informations, reportez-vous à la [Chaîne de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texte *dans le Guide de référence* du protocoleHTTP.

## Par défaut {#section-7ee879762130467199745f2abc662f1e}

Aucune

## Voir aussi {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , de chaînes de [texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
