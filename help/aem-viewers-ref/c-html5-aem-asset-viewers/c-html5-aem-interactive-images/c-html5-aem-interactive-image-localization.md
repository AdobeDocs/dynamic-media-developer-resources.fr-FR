---
title: Localisation des éléments de l’interface utilisateur
description: Certains contenus affichés par la visionneuse d’images interactives sont sujets à localisation. Ce contenu comprend des info-bulles d’élément d’interface utilisateur et un message d’information affiché par la vue de zoom déroulante au chargement.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse d’images interactives sont sujets à localisation. Ce contenu comprend des info-bulles d’élément d’interface utilisateur et un message d’information affiché par la vue de zoom déroulante au chargement.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par l’identificateur spécial SDK de la visionneuse appelé SYMBOL. Tout SYMBOL a une valeur de texte associée par défaut pour un paramètre régional anglais ( `"en"`) fourni avec la visionneuse prête à l’emploi, et peut avoir des valeurs définies par l’utilisateur définies pour autant de paramètres régionaux que nécessaire.

Lorsque la visionneuse démarre, elle vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOLE pris en charge pour ce paramètre régional. Si c’est le cas, elle utilise la valeur définie par l’utilisateur ; Sinon, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises à la visionneuse en tant qu’objet JSON de localisation. Cet objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple d’objet de localisation :

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
   <td colname="col1"> <p> <span class="codeph"> Conteneur.ÉTIQUETTE </span> </p> </td> 
   <td colname="col2"> <p>Étiquette ARIA pour l’élément de visionneuse de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant Vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation d’ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
 </tbody> 
</table>
