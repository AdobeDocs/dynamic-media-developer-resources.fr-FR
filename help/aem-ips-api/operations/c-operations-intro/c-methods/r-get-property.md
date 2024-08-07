---
description: Obtient les valeurs string des propriétés système liées à Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 10%

---

# getProperty{#getproperty}

Obtient les valeurs string des propriétés système liées à Image Portal.

Les propriétés système prises en charge sont les suivantes :

* `IpsVersion` : numéro de version IPS.
* `IpsImageServerUrl` : préfixe d’URL externe complet pour le serveur d’images IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl` : préfixe d’URL pour le rendu des ressources du SVG.
* `SvgRenderEnabled` : valeur True si les ressources du SVG peuvent être rendues par `SvgRenderRootUrl`.

* `UploadPostMaxFileSize` : taille maximale (en octets) des données de fichier autorisées dans un téléchargement [!DNL POST]. Le système rejette les fichiers dont la taille est supérieure à la limite maximale.

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
| nom | `xsd:string` | Oui | Nom de la propriété à obtenir. |

**Sortie (getPropertyReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| valeur | `xsd:string` | Oui | La valeur de la propriété. |

## Exemples {#section-3f80a78dd60c404181b34d3a912d7a36}

Cet exemple de code utilise une constante de chaîne Propriétés IPS pour renvoyer une valeur spécifique. Dans cet exemple, la propriété IPS est la version du serveur IPS.

**Requête**

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
