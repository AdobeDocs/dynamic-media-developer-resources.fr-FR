---
description: Certains contenus affichés par la visionneuse d’images interactive sont soumis à des  de. Cela inclut les info-bulles des éléments de l’interface utilisateur et un message d’information affiché par le de zoom déroulant  au chargement.
seo-description: Certains contenus affichés par la visionneuse d’images interactive sont soumis à des  de. Cela inclut les info-bulles des éléments de l’interface utilisateur et un message d’information affiché par le de zoom déroulant  au chargement.
seo-title: ' des éléments de l’interface utilisateur'
title: ' des éléments de l’interface utilisateur'
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


#  des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse d’images interactive sont soumis à des  de. Cela inclut les info-bulles des éléments de l’interface utilisateur et un message d’information affiché par le de zoom déroulant  au chargement.

Chaque contenu textuel du lecteur pouvant être localisé est représenté par l’identifiant spécial du kit de développement de visionneuse appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour un paramètre régional en anglais ( `"en"`) fourni avec le lecteur prêt à l’emploi et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque le du lecteur , il vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour ces paramètres régionaux. Dans le cas contraire, elle utilise la valeur définie par l’utilisateur ; dans le cas contraire, il revient au texte par défaut prêt à l’emploi.

Les données de  définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de . Cet objet contient le  des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple de cet objet  :

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

Dans l’exemple ci-dessus, l’objet  de définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit un  pour deux éléments d’interface utilisateur dans chaque paramètre régional.

Le code de la page Web doit transmettre l’objet  du au constructeur de la visionneuse, sous la forme d’une valeur de `localizedTexts` champ de l’objet de configuration. Une autre option consiste à transmettre l’objet  en appelant `setLocalizedTexts(localizationInfo)` la méthode.

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
   <td colname="col1"> <p> <span class="codeph"> .ÉTIQUETTE </span> </p> </td> 
   <td colname="col2"> <p>Libellé ARIA pour l’élément de lecteur de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant  principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
 </tbody> 
</table>

