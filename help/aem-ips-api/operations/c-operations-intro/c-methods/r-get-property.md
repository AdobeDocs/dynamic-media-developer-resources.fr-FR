---
description: Obtient des valeurs de chaîne des propriétés système liées au portail d’images.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
TQID: 'https://experienceleague.adobe.com/loaZvP3tI8neQ6ziLR-xKkkNqGGjD8Mq1jbeC8mJEQo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 10%

---

# getProperty{#getproperty}

Obtient des valeurs de chaîne des propriétés système liées au portail d’images.

Les propriétés système prises en charge sont les suivantes :

* `IpsVersion` : numéro de version IPS.
* `IpsImageServerUrl` : préfixe URL externe complet pour le serveur d’images IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl` : préfixe d’URL pour le rendu des ressources SVG.
* `SvgRenderEnabled` : valeur true si les ressources SVG peuvent être rendues par `SvgRenderRootUrl`.

* `UploadPostMaxFileSize` : taille maximale (en octets) des données de fichier autorisée dans un [!DNL POST] de chargement. Le système rejette les fichiers dont la taille est supérieure à la limite maximale.

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

**Input (getPropertyParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| nom | `xsd:string` | Oui | Nom de la propriété à obtenir. |

**Output (getPropertyReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| valeur | `xsd:string` | Oui | Valeur de la propriété . |

## Exemples {#section-3f80a78dd60c404181b34d3a912d7a36}

Cet exemple de code utilise une constante de chaîne Propriétés IPS pour renvoyer une valeur spécifique. Dans cet exemple, la propriété IPS correspond à la version du serveur IPS.

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
