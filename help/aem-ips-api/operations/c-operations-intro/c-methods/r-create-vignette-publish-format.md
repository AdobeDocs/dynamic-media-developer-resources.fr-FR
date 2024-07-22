---
description: Crée un nouveau format de publication pour une vignette.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 4%

---

# createVignettePublishFormat{#createvignettepublishformat}

Crée un nouveau format de publication pour une vignette.

Les formats de vignettes spécifient la taille des vignettes publiées et leurs miniatures, ainsi que les niveaux de zoom, les paramètres d’accentuation et la version du fichier des vignettes générées à partir de vignettes principales publiées sur un serveur de rendu d’image à partir d’IPS.

Les nouvelles versions du serveur de rendu d’image peuvent prendre en charge les vignettes pyramidales, ce qui évite d’avoir à définir des formats de vignettes spécifiques pour la publication.

## Types d’utilisateurs autorisés {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Entrée (createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Obligatoire </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gérer la société à laquelle appartient la vignette. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom pour identifier le format de publication de la vignette. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Spécifie la largeur cible en pixels de la vue de vignette obtenue. </p> <p>Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Crée une vignette pyramidale optimisée pour le zoom sur le serveur de rendu d’image. En commençant par la taille maximale définie par les champs Taille de la vignette cible, vous obtenez plusieurs vues de taille dans un seul fichier de sortie de vignette. Chaque taille d’affichage suivante est réduite de moitié jusqu’à ce que la largeur et la hauteur soient inférieures à 128x128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Spécifie la largeur de chaque miniature résultante en pixels. Ce paramètre est facultatif. Laissez le paramètre défini sur zéro pour aucun fichier de miniature. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le format de fichier des vignettes publiées. Si vous disposez d’une nouvelle version de création d’images et d’une version antérieure du serveur de rendu d’images, vous devez spécifier une version de vignette que votre serveur ImageRendering peut lire. Si vous spécifiez une version supérieure, le serveur de rendu d’image ne peut pas lire les vignettes publiées. Définissez cette variable sur zéro pour publier les vignettes à la dernière version. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sharpen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Applique l’accentuation à l’image de l’affichage principal pour chaque taille de vignette publicitaire. L’accentuation peut compenser le flou lors de la mise à l’échelle des vignettes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Le masquage flou numérique est un moyen flexible et puissant d’augmenter la netteté, en particulier dans les images numérisées. Cela contrôle l’ampleur de chaque débordement (le degré d’obscurité et de luminosité des bordures de périphérie). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Affecte la taille des bords à améliorer ou la largeur des bords, de sorte qu’une plus petite radium améliore les détails à plus petite échelle. Des valeurs de rayon plus élevées peuvent provoquer des halos aux bords. Un détail fin nécessite un rayon plus petit, car un détail minuscule de même taille ou plus petit que le rayon est perdu. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Contrôle le changement de luminosité minimal à accentuer ou la distance entre les valeurs tonales adjacentes et avant que le filtre ne fonctionne. Ce paramètre peut accentuer des bords plus prononcés tout en ne modifiant pas les bords plus subtils. La plage autorisée de seuil de 0 à 255. </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (createVignettePublishFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Oui | La poignée du format de vignette créé. |

## Exemples {#section-0564752d439642b9bb8de2903db6de1e}

Ce code crée le format de publication de vignette. La requête de création spécifie un nom, une largeur et une hauteur de cible, ainsi que d’autres valeurs requises.

**Requête**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Réponse**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```
