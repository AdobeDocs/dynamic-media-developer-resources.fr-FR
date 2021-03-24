---
description: Supprime une cible de zoom.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

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
