---
description: Supprime une cible de zoom.
seo-description: Supprime une cible de zoom.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 11%

---


# deleteZoomTarget{#deletezoomtarget}

Supprime une cible de zoom.

## Types d’utilisateur autorisés {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

## Paramètres {#section-225330a45e7a408f8375e084677d9cb1}

**Entrée (deleteZoomTargetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société à laquelle appartient la cible de zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | Oui | Poignée de la cible de zoom à supprimer. |

**Output (deleteZoomTargetParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemple {#section-a35857a5ca884357a879f7ba6cf985fe}

Cet exemple de code supprime une cible de zoom d’une société.

**Request**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Réponse**

Aucune
