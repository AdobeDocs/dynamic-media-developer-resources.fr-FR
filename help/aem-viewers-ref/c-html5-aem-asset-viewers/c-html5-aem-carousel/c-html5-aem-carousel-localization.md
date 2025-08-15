---
title: Localisation des éléments de l’interface utilisateur
description: Certains contenus affichés par la visionneuse de carrousel sont sujets à localisation. Ce contenu comprend des boutons de navigation par diapositive.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse de carrousel sont sujets à localisation. Ce contenu comprend des boutons de navigation par diapositive.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par l’identificateur spécial SDK de la visionneuse appelé SYMBOL. Tout SYMBOL a une valeur de texte associée par défaut pour un paramètre régional anglais ( `"en"`) fourni avec la visionneuse prête à l’emploi, et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque la visionneuse démarre, elle vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOLE pris en charge pour ce paramètre régional. Si c’est le cas, elle utilise la valeur définie par l’utilisateur ; Sinon, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises à la visionneuse en tant qu’objet JSON de localisation. Cet objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple d’objet de localisation :

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

Dans l’exemple ci-dessus, l’objet de localisation définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit la localisation de deux éléments d’interface utilisateur dans chaque langue.

Le code de la page Web doit transmettre l’objet de localisation au constructeur de la visionneuse, en tant que valeur de champ de `localizedTexts` l’objet de configuration. Une autre option consiste à transmettre l’objet de localisation en appelant `setLocalizedTexts(localizationInfo)` la méthode.

Les SYMBOLES suivants sont pris en charge :

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOLE </p> </th> 
   <th colname="col2" class="entry"> <p>Info-bulle pour... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>État du bouton de pause de lecture sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>État du bouton de pause de lecture désélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Info-bulle et étiquette ARIA pour les boutons des diapositives précédent et suivant. </p> <p>Accepte deux jetons de remplacement : <span class="codeph"> $CURRENT_FRAME$ </span> pour l’index des diapositives en cours et <span class="codeph"> $TOTAL_FRAMES$ </span> pour le nombre total de diapositives. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Conteneur.ÉTIQUETTE </span> </p> </td> 
   <td colname="col2"> <p> Étiquette ARIA pour l’élément de visionneuse de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> Description du rôle ARIA pour le composant Vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> Conseils d’utilisation d’ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
 </tbody> 
</table>
