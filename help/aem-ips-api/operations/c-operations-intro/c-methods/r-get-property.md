---
description: Obtient les valeurs de chaîne des propriétés système liées à Image Portal.
seo-description: Obtient les valeurs de chaîne des propriétés système liées à Image Portal.
seo-title: getProperty
solution: Experience Manager
title: getProperty
topic: Scene7 Image Production System API
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 10%

---


# getProperty{#getproperty}

Obtient les valeurs de chaîne des propriétés système liées à Image Portal.

Les propriétés système prises en charge sont les suivantes :

* `IpsVersion`: Numéro de version IPS.
* `IpsImageServerUrl`: Préfixe d’URL externe complet pour le serveur d’images IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: Préfixe d’URL pour le rendu des fichiers SVG.
* `SvgRenderEnabled`: True si les fichiers SVG peuvent être rendus par  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Taille maximale (en octets) des données de fichier autorisées dans un transfert  [!DNL POST]. Le système rejette les fichiers dont la taille est supérieure à la limite maximale.

## Types d’utilisateur autorisés {#section-2cd36bbd46ed414b8753569d5895530e}

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
| ` *`name`*` | `xsd:string` | Oui | Nom de la propriété à obtenir. |

**Output (getPropertyReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`value`*` | `xsd:string` | Oui | Valeur de la propriété. |

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

