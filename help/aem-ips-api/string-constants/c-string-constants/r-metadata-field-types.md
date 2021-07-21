---
description: Utilisé par MetadataField/type, saveMetadataFieldParam/fieldType et createMetadataField/fieldType.
solution: Experience Manager
title: Types de champ de métadonnées
feature: Dynamic Media Classic,SDK/API,Métadonnées
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# Types de champ de métadonnées{#metadata-field-types}

Utilisé par MetadataField/type, saveMetadataFieldParam/fieldType et createMetadataField/fieldType.

Syntaxe

## Valeurs {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Cas spécial de  [!DNL `SingleFixedTag`] avec un dictionnaire non modifiable initialisé aux valeurs  [!DNL `True`] et  [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Zéro ou plusieurs valeurs string d’un dictionnaire fermé. Seuls les utilisateurs administrateurs peuvent modifier le dictionnaire.
* [!DNL `MultiTag`]: Zéro ou plusieurs valeurs de chaîne.
* [!DNL `SingleFixedTag`]: Une seule valeur string d’un dictionnaire fermé. Si `setAssetMetadata` ou `batchSetAssetMetadata` sont appelés avec une valeur qui n’est pas dans le dictionnaire, une erreur est renvoyée. Seuls les utilisateurs administrateurs peuvent modifier le dictionnaire.

* [!DNL `SingleTag`]: Toute valeur de chaîne unique.
* [!DNL `String`]
