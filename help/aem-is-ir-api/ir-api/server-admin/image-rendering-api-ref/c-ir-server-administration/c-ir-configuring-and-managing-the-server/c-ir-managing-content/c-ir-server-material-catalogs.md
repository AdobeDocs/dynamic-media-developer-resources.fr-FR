---
description: Les catalogues de matériaux fournissent de nombreux paramètres de configuration de rendu d'image.
solution: Experience Manager
title: Catalogues de matières
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# Catalogues de matières{#material-catalogs}

Les catalogues de matériaux fournissent de nombreux paramètres de configuration de rendu d&#39;image.

Les catalogues de matériaux mappent la vignette et les ID de matériaux utilisés dans les demandes aux chemins d&#39;accès aux fichiers réels, peuvent stocker toutes les métadonnées associées aux matériaux et fournir des conteneurs pour les modèles. Ils effectuent le suivi des profils ICC et des macros de commande.

Les catalogues de matériaux sont accessibles uniquement par le composant Java du rendu d’image (co-situé avec le [!DNL Platform Server]). Les fichiers d’attributs de catalogue doivent comporter un suffixe [!DNL .ini] et être placés dans le dossier de catalogue enregistré ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Le catalogue de matériaux par défaut ( [!DNL default.ini]) doit toujours être présent et doit être renseigné avec tous les attributs pour le bon fonctionnement de la diffusion d’images.

