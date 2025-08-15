---
description: Les catalogues de matériaux fournissent de nombreux paramètres de configuration de rendu d'image.
solution: Experience Manager
title: Catalogues de matières
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Catalogues de matières{#material-catalogs}

Les catalogues de matériaux fournissent de nombreux paramètres de configuration de rendu d&#39;image.

Les catalogues de matériaux mappent la vignette et les ID de matériaux utilisés dans les demandes aux chemins d&#39;accès aux fichiers réels, peuvent stocker toutes les métadonnées associées aux matériaux et fournir des conteneurs pour les modèles. Ils effectuent le suivi des profils ICC et des macros de commande.

Les catalogues de matériaux sont accessibles uniquement par le composant Java du rendu d’image (co-situé avec le [!DNL Platform Server]). Les fichiers d’attributs de catalogue doivent comporter un suffixe [!DNL .ini] et être placés dans le dossier de catalogue enregistré ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Le catalogue de matériaux par défaut ( [!DNL default.ini]) doit toujours être présent et doit être renseigné avec tous les attributs pour le bon fonctionnement de la diffusion d’images.
