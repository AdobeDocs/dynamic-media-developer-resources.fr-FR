---
description: Permet d’effacer les fichiers de la corbeille IPS.
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Permet d’effacer les fichiers de la corbeille IPS.

Les fichiers vivent dans la corbeille jusqu’à ce qu’ils soient vidés manuellement ou jusqu’à ce qu’ils soient supprimés de la corbeille. S&#39;ils sont vidés manuellement, ils vivent dans la Corbeille jusqu&#39;à la prochaine tâche de nettoyage (normalement la nuit), lorsqu&#39;ils sont finalement purgés du système. S&#39;ils sortent de la corbeille, les actifs sont nettoyés dans le cadre de cette même activité de nettoyage. Le délai d’expiration est configurable (la valeur par défaut est de 7 jours).

## Types d’utilisateur autorisés {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Paramètres {#section-8e1fb0ee3aae453581e99ef76e298569}

**Entrée (emptyAssetsFromTrashParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société propriétaire des actifs. |
| `*`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées représentant les éléments à vider de la corbeille. |

**Sortie (emptyAssetsFromTrashParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Oui | Nombre de fichiers vidés avec succès de la corbeille. |
| `*`warningCount`*` | `xsd:Int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de vider des ressources de la corbeille. |
| `*`errorCount`*` | `xsd:Int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de vider des fichiers de la corbeille. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté de les vider de la corbeille. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté de les vider de la corbeille. |

## Exemples {#section-6154a873b6c342bf92e2036280cafdcf}

Cet exemple de code utilise le handle de la société et un tableau de descripteurs de ressources qui contient des poignées vers les ressources à vider de la corbeille.

**Request**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Réponse**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

