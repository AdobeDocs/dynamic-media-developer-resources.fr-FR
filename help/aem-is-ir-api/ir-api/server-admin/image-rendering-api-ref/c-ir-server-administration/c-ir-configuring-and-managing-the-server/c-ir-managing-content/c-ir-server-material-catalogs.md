---
description: Les catalogues de matériaux offrent de nombreux paramètres de configuration de rendu d’image.
seo-description: Les catalogues de matériaux offrent de nombreux paramètres de configuration de rendu d’image.
seo-title: Catalogues de matières
solution: Experience Manager
title: Catalogues de matières
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# Catalogues de matériaux{#material-catalogs}

Les catalogues de matériaux offrent de nombreux paramètres de configuration de rendu d’image.

Les catalogues de matériaux mappent les vignettes et les identifiants de matériaux utilisés dans les requêtes aux chemins d’accès réels aux fichiers, peuvent stocker toutes les métadonnées associées aux matériaux et fournir des conteneurs pour les modèles. Ils conservent la trace des profils ICC et des macros de commande.

Les catalogues de matériaux sont accessibles uniquement par le composant Java de Image Rendering (colocalisé avec Platform Server). Les fichiers d’attributs du catalogue doivent avoir un suffixe [!DNL .ini] et être placés dans le dossier de catalogue enregistré ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Le catalogue de matières par défaut ( [!DNL default.ini]) doit toujours être présent et doit être renseigné avec tous les attributs pour que la diffusion d’images fonctionne correctement.
