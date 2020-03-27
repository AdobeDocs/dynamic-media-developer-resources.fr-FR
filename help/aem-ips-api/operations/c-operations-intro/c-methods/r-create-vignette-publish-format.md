---
description: Crée un nouveau format de publication pour une vignette.
seo-description: Crée un nouveau format de publication pour une vignette.
seo-title: createVideoPublishFormat
solution: Experience Manager
title: createVideoPublishFormat
topic: Scene7 Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createVideoPublishFormat{#createvignettepublishformat}

Crée un nouveau format de publication pour une vignette.

Les formats de vignette indiquent la taille des vignettes publiées et leurs miniatures, ainsi que les niveaux de zoom, les paramètres d’accentuation et la version de format de fichier des vignettes générées à partir de vignettes originales publiées sur un serveur de rendu d’images à partir d’IPS.

Les versions plus récentes du serveur de rendu d’images peuvent prendre en charge les vignettes pyramidales, ce qui évite d’avoir à définir des formats de vignettes spécifiques pour la publication.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Traitement du auquel appartient la vignette. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom permettant d’identifier le format de publication de vignettes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Indique la largeur de  du de vignette résultant, en pixels. </p> <p>Utilisez zéro pour que la vignette de sortie ait la même taille que la vignette originale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Crée une vignette pyramidale optimisée pour le zoom sur le serveur Image Rendering. En commençant à la taille maximale, comme défini dans les champs Taille de vignette cible, il est possible de créer des vues de taille multiple dans un même fichier cible de vignette. Chaque taille de vue suivante sera diminuée de moitié jusqu'à ce que la largeur et la hauteur soient comprises dans un format 128 x 128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique la largeur de chaque miniature obtenue en pixels. Ce paramètre est facultatif. Conservez la valeur zéro pour aucun fichier miniature. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pouceLargeur</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le format de fichier des vignettes publiées. Avec une nouvelle version de Image Authoring et une ancienne version du serveur de rendu d’images, vous devez spécifier une version de vignette que votre serveur ImageRendering peut lire. Si vous spécifiez une version supérieure, le serveur de rendu d’images ne peut pas lire les vignettes publiées. Définissez cette valeur sur zéro pour publier les vignettes à la dernière version. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Indique le caractère qui sépare le nom de la vignette et le suffixe indiquant sa largeur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accentuation</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Applique l’accentuation à l’image  principale du pour chaque taille de vignette publicitaire. L’accentuation peut compenser le flou lors de l’échelle des vignettes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Le masquage flou numérique est un moyen flexible et puissant d’augmenter la netteté, en particulier dans les images numérisées. Cela contrôle l'amplitude de chaque dépassement (le degré de foncement et de luminosité des bordures du bord). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Affecte la taille des bords à améliorer ou la largeur des bords, de sorte qu’un rayon plus petit améliore les détails à plus petite échelle. Des valeurs de rayon plus élevées peuvent provoquer des halos aux bords. Les détails fins nécessitent un rayon plus petit, car des détails minuscules de même taille ou plus petits que le rayon sont perdus. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Expression de code </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Contrôle le changement de luminosité minimal à accentuer ou la distance entre les valeurs tonales adjacentes avant le fonctionnement du filtre. Ce paramètre permet d’accentuer les bords plus prononcés tout en laissant les bords plus subtils intacts. Plage de seuil autorisée de 0 à 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Oui | Poignée du format de vignette créé. |

## Exemples {#section-0564752d439642b9bb8de2903db6de1e}

Ce code crée un format de publication de vignette. La demande de création spécifie un nom, une largeur et une hauteur  le nom, ainsi que d’autres valeurs requises.

**Request**

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

