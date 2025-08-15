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

Les formats de vignettes spécifient la taille des vignettes publiées et de leurs miniatures, ainsi que les niveaux de zoom, les paramètres d’accentuation et la version du format de fichier pour les vignettes produites à partir des vignettes principales publiées sur un serveur de rendu d’images à partir d’IPS.

Les nouvelles versions du serveur de rendu d’images peuvent prendre en charge les vignettes pyramidales, ce qui élimine la nécessité de définir des tailles de format de vignette spécifiques pour la publication.

## Types d’utilisateurs autorisés {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Input (createVignettePublishFormatParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gérer à la société à laquelle appartient la vignette. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom permettant d’identifier le format de publication de la vignette. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Indique la largeur cible de la vue de vignette résultante en pixels. </p> <p>Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Crée une vignette pyramidale optimisée pour le zoom sur le serveur de rendu d’image. À partir de la taille maximale, définie par les champs Taille de la vignette cible , cela crée plusieurs vues de taille dans un seul fichier de sortie de vignette. Chaque taille d’affichage suivante est divisée par deux jusqu’à ce que la largeur et la hauteur fassent moins de 128 x 128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique la largeur de chaque miniature résultante en pixels. Ce paramètre est facultatif. Laissez le champ sur zéro pour aucun fichier de miniature. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le format de fichier des vignettes publiées. Étant donné une nouvelle version de la création d’images et une ancienne version du serveur de rendu d’images, vous devez spécifier une version de vignette que votre serveur de rendu d’images peut lire. Si vous spécifiez une version supérieure, le serveur de rendu d’image ne peut pas lire les vignettes publiées. Définissez cette valeur sur zéro pour publier des vignettes à la version la plus récente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accentuer </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Applique un accentuation à l’image de la vue principale pour chaque taille de vignette de publication L’accentuation peut compenser le flou lorsque les vignettes sont mises à l’échelle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Le masquage flou numérique est un moyen flexible et puissant d’augmenter la netteté, en particulier dans les images numérisées. Cette option permet de contrôler l'ampleur de chaque dépassement (l'intensité d'obscurcissement et de luminosité des bordures). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Affecte la taille des arêtes à améliorer ou la largeur des arêtes, de sorte qu'un rayon plus petit améliore le détail à plus petite échelle. Des valeurs de rayon plus élevées peuvent provoquer des halos sur les arêtes. Le détail fin nécessite un rayon plus petit, car un détail minuscule de la même taille ou inférieur au rayon est perdu. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> l’expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Contrôle la modification de luminosité minimale à accentuer ou l’écart minimal requis entre les valeurs tonales adjacentes avant le fonctionnement du filtre. Ce paramètre permet d’accentuer les contours plus prononcés tout en laissant les contours plus subtils intacts. La plage autorisée de seuil de 0 à 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Oui | Poignée au format de vignette créé. |

## Exemples {#section-0564752d439642b9bb8de2903db6de1e}

Ce code crée le format de publication de vignette. La demande de création spécifie un nom, la largeur et la hauteur de la cible, ainsi que d’autres valeurs requises.

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
