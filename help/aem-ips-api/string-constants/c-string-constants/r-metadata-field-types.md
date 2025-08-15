---
description: Utilisé par MetadataField/type, saveMetadataFieldParam/fieldType et createMetadataField/fieldType.
solution: Experience Manager
title: Types de champs de métadonnées
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# Types de champs de métadonnées{#metadata-field-types}

Utilisé par MetadataField/type, saveMetadataFieldParam/fieldType et createMetadataField/fieldType.

Syntaxe

## Valeurs {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: un cas particulier de [!DNL `SingleFixedTag`] avec un dictionnaire non modifiable initialisé aux valeurs [!DNL `True`] et [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: zéro ou plusieurs valeurs de chaîne d’un dictionnaire fermé. Seuls les utilisateurs administrateurs peuvent modifier le dictionnaire.
* [!DNL `MultiTag`]: zéro ou plusieurs valeurs de chaîne.
* [!DNL `SingleFixedTag`]: valeur de chaîne unique d’un dictionnaire fermé. Si `setAssetMetadata` ou `batchSetAssetMetadata` sont appelés avec une valeur qui ne figure pas dans le dictionnaire, une erreur est renvoyée. Seuls les utilisateurs administrateurs peuvent modifier le dictionnaire.

* [!DNL `SingleTag`]: n’importe quelle valeur de chaîne.
* [!DNL `String`]
