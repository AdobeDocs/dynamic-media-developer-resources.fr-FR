---
description: Utilisé par MetadataField/type, saveMetadataFieldParam/fieldType et createMetadataField/fieldType.
solution: Experience Manager
title: Types de champs de métadonnées
feature: Dynamic Media Classic, SDK/API, Métadonnées
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# Types de champs de métadonnées{#metadata-field-types}

Utilisé par MetadataField/type, saveMetadataFieldParam/fieldType et createMetadataField/fieldType.

Syntaxe

## Valeurs {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Cas spécial de  [!DNL `SingleFixedTag`] avec un dictionnaire non modifiable initialisé aux valeurs  [!DNL `True`] et  [!DNL `False`]et.

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Zéro ou plusieurs valeurs de chaîne d’un dictionnaire fermé. Seuls les administrateurs peuvent modifier le dictionnaire.
* [!DNL `MultiTag`]: Zéro ou plusieurs valeurs de chaîne.
* [!DNL `SingleFixedTag`]: Valeur de chaîne unique issue d’un dictionnaire fermé. Si `setAssetMetadata` ou `batchSetAssetMetadata` sont appelés avec une valeur qui ne figure pas dans le dictionnaire, une erreur est renvoyée. Seuls les administrateurs peuvent modifier le dictionnaire.

* [!DNL `SingleTag`]: Toute valeur de chaîne unique.
* [!DNL `String`]

