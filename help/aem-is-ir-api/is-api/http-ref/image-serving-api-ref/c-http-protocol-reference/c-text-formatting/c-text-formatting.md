---
description: Image Serving fournit plusieurs alternatives pour le rendu du texte, accessibles avec les commandes text= et textPs=.
solution: Experience Manager
title: Formatage de texte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 6%

---

# Formatage de texte{#text-formatting}

Image Serving fournit plusieurs alternatives pour le rendu du texte, accessibles avec les commandes text= et textPs=.

`textPs=` Offre un haut niveau de similitude avec le rendu de texte avec Adobe Photoshop et Illustrator. `text=` est raisonnablement compatible avec le texte rendu avec le Bloc-notes Windows.

>[!NOTE]
>
>Outre les différences répertoriées ailleurs, `text=` produit des différences subtiles dans le texte rendu par rapport à `textPs=`. Par exemple, les soulignements n’ont pas la même épaisseur et la même position et les italiques synthétisés sont rendus à un angle légèrement différent. Si le texte ne rentre pas dans l’espace disponible, `text=` peut partiellement rogner la dernière ligne, tout en `textPs=` ne rendant que des lignes complètes.

Toutes les commandes de texte acceptent le texte formaté basé sur un sous-ensemble de la spécification RTF (Rich Text Format). Chaque calque de texte peut spécifier une commande de texte différente.

Le tableau suivant répertorie les principales fonctionnalités disponibles pour chaque commande de texte :

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Caractéristique</b> </th> 
   <th class="entry"> <b> texte=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Voir aussi</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop compatible </p> </td> 
   <td> <p> non </p> </td> 
   <td> <p> limité </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Enchaînement du texte dans des formes arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Enchaînement du texte le long de tracés arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ajustement de copie </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Ajustement de copie <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Marges des zones de texte </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justification complète du paragraphe </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justification de la dernière ligne </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mise en retrait de paragraphe </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Texte en lettres capitales et petites capitales </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Couleurs du service d’images </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\*\iscolortable </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Plusieurs modes de lissage des gris </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flux de texte haut-bas/droite-gauche </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Prise en charge des photopolices® </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Gestion des polices </td> 
  </tr> 
  <tr> 
   <td> <p>Ajuster le calque au texte </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Prise en charge CMJN </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flux de caractères de droite à gauche </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Désactiver le retour automatique à la ligne </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mise à l’échelle automatique du texte pour l’adapter au calque (en modifiant la résolution) </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Les chaînes compatibles RTF peuvent être assemblées manuellement ou en formatant le texte souhaité dans un éditeur de texte ou un traitement de texte capable d’enregistrer les fichiers RTF. Le fichier RTF peut ensuite être ouvert dans un éditeur de texte brut et le contenu RTF brut correspondant du fichier peut être copié dans l’URL de requête.

Certains traitements de texte génèrent des fichiers assez volumineux, qui comprennent des préambules substantiels qui ne sont pas utilisés par Dynamic Media serveur d’images. Il est recommandé de supprimer les éléments RTF inutilisés de la chaîne avant de passer la chaîne aux commandes de texte.

Le codage de langage basé sur les normes UTF-8 et ISO est pris en charge dans les chaînes RTF comme alternative aux mécanismes de codage de caractères RTF standard. Cela permet aux applications d’envoyer du texte non anglais au serveur sans connaissance du codage RTF.

Tous les caractères non compatibles HTTP doivent être correctement échappés, si la chaîne doit être transmise via http. Seules &#39;=&#39;, &#39;&amp;&#39; et &#39; %&#39; doivent être placées dans une séquence d’échappement si la chaîne est incorporée dans le `catalog::Modifiers` champ d’un enregistrement de catalogue d’images. Les caractères de contrôle, y compris `<CR>`, `<LF>`, et `<TAB>` doivent toujours être supprimés.

Les moteurs de texte Image Serving interprètent un sous-ensemble de commandes définies par la spécification RTF (Rich Text Format), version 1.6. Ce sous-ensemble est axé sur la mise en forme des polices/caractères, la mise en forme simple des paragraphes et la prise en charge des polices et des jeux de caractères internationaux. Les constructions de mise en forme plus avancées, telles que les feuilles de style et les tableaux, ne sont pas prises en charge pour le moment.

Une connaissance de la spécification RTF (Rich Text Format), telle que publiée par Microsoft, est requise lorsque vous tentez de construire manuellement des chaînes de texte codées RTF.

* [Gestion des polices](r-font-handling.md)
* [Gestion des couleurs](r-color-handling.md)
* [Ajustement de copie](r-copy-fitting.md)
* [Calques de texte](r-text-layers.md)
* [Positionnement du texte](r-text-positioning.md)
* [Caractères réservés](r-reserved-characters.md)
* [Commandes RTF et mots-clés pris en charge](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemples de codage RTF](r-rtf-encoding-examples.md)
