---
description: Met à jour les paramètres du format de publication de la vignette.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

Met à jour les paramètres du format de publication de la vignette.

## Types d’utilisateurs autorisés {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignettePublishFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| vignetteFormatHandle | `xsd:string` | Oui | Poignée du format de publication. |
| nom | `xsd:string` | Non | Nom du format de publication. |
| targetWidth | `xsd:int` | Oui | Indique la largeur cible de la vue de vignette résultante en pixels. Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette principale. |
| targetHeight | `xsd:int` | Oui | Indique la hauteur cible de la vue de vignette résultante en pixels. Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette principale. |
| createPyramid | `xsd:boolean` | Oui | Crée une vignette pyramidale optimisée pour le zoom sur le serveur de rendu d’image. À partir de la taille maximale, définie par les champs Taille de la vignette cible , cela crée plusieurs vues de taille dans un seul fichier de sortie de vignette. Chaque taille d’affichage suivante est divisée par deux jusqu’à ce que la largeur et la hauteur fassent moins de 128 x 128 pixels. |
| thumbWidth | `xsd:int` | Oui | Indique la largeur de chaque miniature résultante en pixels. Ce paramètre est facultatif. Laissez le champ sur zéro pour aucun fichier de miniature. |
| saveAsVersion | `xsd:int` | Oui | Indique le format de fichier des vignettes publiées. Étant donné une nouvelle version de la création d’images et une ancienne version du serveur de rendu d’images, vous devez spécifier une version de vignette que votre serveur de rendu d’images peut lire. Si vous spécifiez une version supérieure, le serveur de rendu d’image ne peut pas lire les vignettes publiées. Définissez cette valeur sur zéro pour publier des vignettes à la version la plus récente. |
| sizeSuffixSeparator | `xsd:string` | Oui | Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. |
| aiguiser | `xsd:int` | Non | Applique un accentuage à l’image de la vue principale pour chaque taille de vignette de publication. L’accentuation peut compenser le flou lorsque les vignettes sont mises à l’échelle. |
| usmAmount | `xsd:double` | Oui | Le masquage flou numérique est un moyen flexible et puissant d’augmenter la netteté, en particulier dans les images numérisées. Cette option permet de contrôler l&#39;ampleur de chaque dépassement (l&#39;intensité d&#39;obscurcissement et d&#39;éclaircissement des bordures). |
| usmRadius | `xsd:double` | Oui | Affecte la taille des arêtes à améliorer ou la largeur des arêtes, de sorte qu&#39;un rayon plus petit améliore les détails à plus petite échelle. Des valeurs de rayon plus élevées peuvent provoquer des halos sur les arêtes. Le détail fin nécessite un rayon plus petit, car un détail minuscule de la même taille ou inférieur au rayon est perdu. |
| usmThreshold | `xsd:int` | Oui | Contrôle la modification de luminosité minimale à accentuer ou l’écart minimal requis entre les valeurs tonales adjacentes avant le fonctionnement du filtre. Ce paramètre permet d’accentuer les contours plus prononcés tout en laissant les contours plus subtils intacts. La plage de seuil autorisée est comprise entre 0 et 255. |

**Output (updateVignettePublishFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Oui | Gérez le format de publication de vignette mis à jour. |

## Exemple {#section-fcba4bf2b7264786a676e315a35dbe43}

Cet exemple de code met à jour un format de publication de vignette et renvoie la poignée au format mis à jour.

**Requête**

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
