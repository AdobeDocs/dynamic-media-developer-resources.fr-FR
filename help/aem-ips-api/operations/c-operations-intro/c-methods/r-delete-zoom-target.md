---
description: Supprime un  de zoom.
seo-description: Supprime un  de zoom.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
topic: Scene7 Image Production System API
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteZoomTarget{#deletezoomtarget}

Supprime un  de zoom.

## Types d’utilisateurs autorisés {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture au fichier.

## Paramètres {#section-225330a45e7a408f8375e084677d9cb1}

**Entrée (deleteZoomTargetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du  auquel appartient le de zoom. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Oui | La poignée du de zoom à supprimer . |

**Output (deleteZoomTargetParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemple {#section-a35857a5ca884357a879f7ba6cf985fe}

Cet exemple de code supprime un  de zoom d&#39;un  de.

**Request**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Réponse**

Aucune
