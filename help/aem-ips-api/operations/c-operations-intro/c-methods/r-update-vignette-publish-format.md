---
description: Met à jour les paramètres de format de publication de vignette.
seo-description: Met à jour les paramètres de format de publication de vignette.
seo-title: updateVideoPublishFormat
solution: Experience Manager
title: updateVideoPublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateVideoPublishFormat{#updatevignettepublishformat}

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
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Oui | Poignée de format de publication. |
| ` *`nom`*` | `xsd:string` | Non | Nom du format de publication. |
| ` *`targetWidth`*` | `xsd:int` | Oui | Indique la largeur de  du de vignette résultant, en pixels. Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette originale. |
| ` *`targetHeight`*` | `xsd:int` | Oui | Indique la hauteur de  du de vignettes résultant, en pixels. Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette originale. |
| ` *`createPyramid`*` | `xsd:boolean` | Oui | Crée une vignette pyramidale optimisée pour le zoom sur le serveur Image Rendering. En commençant à la taille maximale, comme défini dans les champs Taille de vignette cible, il est possible de créer des vues de taille multiple dans un même fichier cible de vignette. Chaque taille de vue suivante sera diminuée de moitié jusqu&#39;à ce que la largeur et la hauteur soient comprises dans un format 128 x 128 pixels. |
| ` *`thumbWidth`*` | `xsd:int` | Oui | Indique la largeur de chaque miniature obtenue en pixels. Ce paramètre est facultatif. Conservez la valeur zéro pour aucun fichier miniature. |
| ` *`saveAsVersion`*` | `xsd:int` | Oui | Indique le format de fichier des vignettes publiées. Avec une nouvelle version de Image Authoring et une ancienne version du serveur de rendu d’images, vous devez spécifier une version de vignette lisible par votre serveur ImageRendering. Si vous spécifiez une version supérieure, le serveur de rendu d’images ne peut pas lire les vignettes publiées. Définissez cette valeur sur zéro pour publier les vignettes à la dernière version. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | Oui | Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. |
| ` *`accentuer`*` | `xsd:int` | Non | Applique l’accentuation à l’image  principale du pour chaque taille de vignette de publication. L’accentuation peut compenser le flou lorsque les vignettes sont mises à l’échelle. |
| ` *`usmAmount`*` | `xsd:double` | Oui | Le masquage flou numérique est un moyen flexible et puissant d’augmenter la netteté, en particulier dans les images numérisées. Cela contrôle l’amplitude de chaque dépassement (le degré de noirceur et de luminosité des bordures du bord). |
| ` *`usmRadius`*` | `xsd:double` | Oui | Affecte la taille des bords à améliorer ou la largeur des bords, de sorte qu’un rayon plus petit améliore les détails à petite échelle. Des valeurs de rayon plus élevées peuvent provoquer des halos aux bords. Les détails fins nécessitent un rayon plus petit, car des détails minuscules de même taille ou plus petits que le rayon sont perdus. |
| ` *`usmThreshold`*` | `xsd:int` | Oui | Contrôle le changement de luminosité minimal à accentuer ou la distance entre les valeurs tonales adjacentes avant le fonctionnement du filtre. Ce paramètre permet d’accentuer les bords plus prononcés tout en laissant les bords plus subtils intacts. La plage de seuil autorisée est comprise entre 0 et 255. |

**Output (updateViewettePublishFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Oui | Traitement du format de publication de vignette mis à jour. |

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

