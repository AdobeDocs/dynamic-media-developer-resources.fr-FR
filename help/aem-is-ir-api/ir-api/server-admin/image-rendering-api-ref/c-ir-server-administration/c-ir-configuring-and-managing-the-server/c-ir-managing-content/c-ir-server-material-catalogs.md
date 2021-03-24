---
description: Les catalogues de matériaux offrent de nombreux paramètres de configuration de rendu d’image.
solution: Experience Manager
title: Catalogues de matières
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Catalogues de matériaux{#material-catalogs}

Les catalogues de matériaux offrent de nombreux paramètres de configuration de rendu d’image.

Les catalogues de matériaux mappent les vignettes et les identifiants de matériaux utilisés dans les requêtes aux chemins d’accès réels aux fichiers, peuvent stocker toutes les métadonnées associées aux matériaux et fournir des conteneurs pour les modèles. Ils conservent la trace des profils ICC et des macros de commande.

Les catalogues de matériaux sont accessibles uniquement par le composant Java de Image Rendering (colocalisé avec Platform Server). Les fichiers d’attributs du catalogue doivent avoir un suffixe [!DNL .ini] et être placés dans le dossier de catalogue enregistré ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Le catalogue de matières par défaut ( [!DNL default.ini]) doit toujours être présent et doit être renseigné avec tous les attributs pour que la diffusion d’images fonctionne correctement.
