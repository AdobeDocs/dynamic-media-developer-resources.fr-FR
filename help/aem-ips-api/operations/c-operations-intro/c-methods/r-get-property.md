---
description: Obtient les valeurs string des propriétés système liées à Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 10%

---

# getProperty{#getproperty}

Obtient les valeurs string des propriétés système liées à Image Portal.

Les propriétés système prises en charge sont les suivantes :

* `IpsVersion`: Numéro de version IPS.
* `IpsImageServerUrl`: Préfixe d’URL externe complet pour le serveur d’images IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: Préfixe d’URL pour le rendu des ressources SVG.
* `SvgRenderEnabled`: True si les ressources SVG peuvent être générées par  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Taille maximale (en octets) des données de fichier autorisées dans un chargement  [!DNL POST]. Le système rejette les fichiers dont la taille est supérieure à la limite maximale.

## Types d’utilisateurs autorisés {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Entrée (getPropertyParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`name`*` | `xsd:string` | Oui | Nom de la propriété à obtenir. |

**Sortie (getPropertyReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`value`*` | `xsd:string` | Oui | La valeur de la propriété. |

## Exemples {#section-3f80a78dd60c404181b34d3a912d7a36}

Cet exemple de code utilise une constante de chaîne Propriétés IPS pour renvoyer une valeur spécifique. Dans cet exemple, la propriété IPS est la version du serveur IPS.

**Request**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Réponse**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
