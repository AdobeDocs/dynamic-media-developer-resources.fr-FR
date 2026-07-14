---
description: Cible d’une action de clic dans le navigateur.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

Cible d’une action de clic dans le navigateur.

Toujours associé à une image. Vous pouvez obtenir une cible `ImageMap` à partir de `ImageInfo`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| imageMapHandle | `xsd:string` | Identifiant de zone cliquable. |
| [!DNL name] | `xsd:string` | Nom de la zone cliquable. |
| [!DNL region] | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur l’attribut de balise HTML `<area>`. |
| [!DNL action] | `xsd:string` | Autres attributs à inclure dans la balise `<area>` HTML, dont l’URL `href`. |
| typeForme | `xsd:boolean` | Valeur [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Position au format de l’attribut [!DNL coords] de l’élément de `<area>` HTML. Par exemple : `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True si la zone cliquable est activée. |
| lastModified | `xsd:dateTime` | Date et heure de la dernière modification de la zone cliquable. |

