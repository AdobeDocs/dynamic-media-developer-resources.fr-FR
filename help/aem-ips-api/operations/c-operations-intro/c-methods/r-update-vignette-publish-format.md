---
description: Met à jour les paramètres de format de publication de vignette.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 20%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

Met à jour les paramètres de format de publication de vignette.

## Types d’utilisateurs autorisés {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Entrée (updateViewPublishFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Oui | Poignée du format de publication. |
| `*`name`*` | `xsd:string` | Non | Nom du format de publication. |
| `*`targetWidth`*` | `xsd:int` | Oui | Spécifie la largeur cible en pixels de la vue de vignette obtenue. Utilisez zéro pour que la vignette de sortie ait la même taille que la Principale vignette. |
| `*`targetHeight`*` | `xsd:int` | Oui | Indique la hauteur cible en pixels de la vue de vignette obtenue. Utilisez zéro pour que la vignette de sortie ait la même taille que la Principale vignette. |
| `*`createPyramid`*` | `xsd:boolean` | Oui | Crée une vignette pyramidale optimisée pour le zoom sur le serveur Image Rendering. En commençant à la taille maximale, comme défini dans les champs Taille de vignette cible, il est possible de créer des vues de taille multiple dans un même fichier cible de vignette. Chaque taille de vue suivante sera diminuée de moitié jusqu&#39;à ce que la largeur et la hauteur soient comprises dans un format 128 x 128 pixels. |
| `*`thumbWidth`*` | `xsd:int` | Oui | Spécifie la largeur de chaque miniature résultante en pixels. Ce paramètre est facultatif. Laissez le paramètre défini sur zéro pour aucun fichier de miniature. |
| `*`saveAsVersion`*` | `xsd:int` | Oui | Indique le format de fichier des vignettes publiées. Si vous disposez d’une nouvelle version de la création d’images et d’une ancienne version du serveur de rendu d’images, vous devez spécifier une version de vignette que votre serveur ImageRendering peut lire. Si vous spécifiez une version supérieure, le serveur de rendu d’image ne peut pas lire les vignettes publiées. Définissez cette variable sur zéro pour publier les vignettes à la dernière version. |
| `*`sizeSuffixSeparator`*` | `xsd:string` | Oui | Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. |
| `*`accentuer`*` | `xsd:int` | Non | Applique l’accentuation à l’image de l’affichage principal pour chaque taille de vignette de publication. L’accentuation peut compenser le flou lorsque les vignettes sont mises à l’échelle. |
| `*`usmAmount`*` | `xsd:double` | Oui | Le masquage flou numérique est un moyen flexible et puissant d’augmenter la netteté, en particulier dans les images numérisées. Cela contrôle l’ampleur de chaque débordement (plus les bordures des bords deviennent sombres et plus légères). |
| `*`usmRadius`*` | `xsd:double` | Oui | Affecte la taille des bords à améliorer ou la largeur des bords, de sorte qu’un rayon plus petit augmente les détails à plus petite échelle. Des valeurs de rayon plus élevées peuvent provoquer des halos aux bords. Un détail fin nécessite un rayon plus petit, car un détail minuscule de même taille ou plus petit que le rayon est perdu. |
| `*`usmThreshold`*` | `xsd:int` | Oui | Contrôle le changement de luminosité minimal à accentuer ou la distance entre les valeurs tonales adjacentes et avant que le filtre ne fonctionne. Ce paramètre peut accentuer des bords plus prononcés tout en ne modifiant pas les bords plus subtils. La plage de seuil autorisée est comprise entre 0 et 255. |

**Sortie (updateViewPublishFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Oui | Gérer au format de publication de vignette mis à jour. |

## Exemple {#section-fcba4bf2b7264786a676e315a35dbe43}

Cet exemple de code met à jour le format de publication d’une vignette et renvoie la poignée au format mis à jour.

**Request**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Réponse**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
