---
title: emptyAssetsFromTrash
description: Empêche les ressources de la corbeille IPS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 7%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Empêche les ressources de la corbeille IPS.

Assets vit dans la corbeille jusqu’à ce qu’elle soit vidée manuellement ou jusqu’à ce qu’elle sorte de la corbeille. S’ils sont vidés manuellement, ils vivent dans la corbeille jusqu’à la prochaine tâche de nettoyage (normalement de nuit), lorsqu’ils sont finalement purgés du système. S’ils expirent de la corbeille, les ressources sont nettoyées dans le cadre de cette même activité de nettoyage. Le délai d’expiration est configurable (la valeur par défaut est de 7 jours).

## Types d’utilisateurs autorisés {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | xsd:string | Oui | Gestionnaire de l’entreprise propriétaire des actifs. |
| assetHandleArray | types:HandleArray | Oui | Tableau de poignées représentant les éléments à vider de la corbeille. |

**Sortie (emptyAssetsFromTrashParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | xsd:Int | Oui | Nombre de ressources vidées de la corbeille avec succès. |
| warningCount | xsd:Int | Oui | Nombre d’avertissements générés lorsque l’opération tentait de vider des ressources de la corbeille. |
| errorCount | xsd:Int | Oui | Nombre d’erreurs générées lorsque l’opération tentait de vider des ressources de la corbeille. |
| warningDetailArray | types:AssetOperationFaultArray | Non | Tableau de détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté de les vider de la corbeille. |
| errorDetailArray | types:AssetOperationFaultArray | Non | Tableau de détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté de les vider de la corbeille. |

## Exemples {#section-6154a873b6c342bf92e2036280cafdcf}

Cet exemple de code utilise le gestionnaire de l’entreprise et un tableau de gestionnaires de ressources qui contient des gestionnaires des ressources à vider de la corbeille.

**Requête**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Réponse**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
