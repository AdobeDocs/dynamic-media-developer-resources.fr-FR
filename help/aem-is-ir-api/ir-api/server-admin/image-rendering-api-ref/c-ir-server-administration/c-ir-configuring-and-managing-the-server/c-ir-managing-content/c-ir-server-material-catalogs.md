---
description: Les catalogues de matériaux fournissent de nombreux paramètres de configuration de rendu d’image.
solution: Experience Manager
title: Catalogues de matières
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Catalogues de matières{#material-catalogs}

Les catalogues de matériaux fournissent de nombreux paramètres de configuration de rendu d’image.

Les catalogues de matériaux mappent la vignette et les identifiants de matériau utilisés dans les requêtes aux chemins de fichier réels, peuvent stocker toutes les métadonnées associées aux matériaux et fournir des conteneurs pour les modèles. Ils effectuent le suivi des profils ICC et des macros de commande.

Les catalogues de matériaux sont accessibles uniquement par le composant Java du rendu d’image (colocalisé avec le serveur Platform). Les fichiers d’attributs du catalogue doivent avoir un suffixe [!DNL .ini] et être placés dans le dossier de catalogue enregistré ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Le catalogue de matières par défaut ( [!DNL default.ini]) doit toujours être présent et doit être renseigné avec tous les attributs pour un bon fonctionnement de la diffusion d’images.
