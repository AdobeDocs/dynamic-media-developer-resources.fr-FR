---
description: La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles par les commandes text= et textPs=.
seo-description: La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles par les commandes text= et textPs=.
seo-title: Formatage du texte
solution: Experience Manager
title: Formatage du texte
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Formatage du texte{#text-formatting}

La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles par les commandes text= et textPs=.

`textPs=` offre un niveau élevé de similitude avec le texte rendu avec Adobe Photoshop et Illustrator. `text=` est raisonnablement compatible avec le texte rendu avec le Wordpad Windows.

>[!NOTE]
>
>Outre les différences répertoriées ailleurs, `text=` produit des différences subtiles dans le texte rendu par rapport à `textPs=`. Par exemple, les soulignements n’ont pas la même épaisseur et la même position et les italiques synthétisées sont rendues selon un angle légèrement différent. Si le texte ne tient pas dans l’espace disponible, `text=` peut recadrer partiellement la dernière ligne, alors `textPs=` qu’il ne rendra que les lignes complètes.

Toutes les commandes de texte acceptent le texte formaté en fonction d’un sous-ensemble de la spécification RTF (Rich Text Format). Chaque calque de texte peut spécifier une commande de texte différente.

Le tableau suivant  les principales fonctionnalités disponibles pour chaque commande de texte :

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Fonctionnalité</b> </th> 
   <th class="entry"> <b> texte=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Voir aussi</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Compatible avec Adobe Photoshop </p> </td> 
   <td> <p> non </p> </td> 
   <td> <p> limité </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Transformer le texte en formes arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flux de texte le long de chemins arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Copier-ajuster </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Copie-ajustement <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Marges de zone de texte </p> </td> 
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
   <td> <p>justification de la dernière ligne </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Retrait de paragraphe </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tout en majuscules et petit texte en majuscules </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Couleurs de diffusion d’images </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Plusieurs modes de lissage </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>enchaînement de texte supérieur inférieur/droit-gauche </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Prise en charge de Photofont® </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Gestion des polices </td> 
  </tr> 
  <tr> 
   <td> <p>Ajuster automatiquement le calque au texte </p> </td> 
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
   <td> <p>Désactiver le retour à la ligne </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mise à l’échelle automatique du texte en fonction du calque (selon une résolution variable) </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Les chaînes conformes RTF peuvent être assemblées manuellement ou en formatant le texte souhaité dans un éditeur de texte ou un traitement de texte capable d’enregistrer des fichiers RTF. Le fichier RTF peut alors être ouvert dans un éditeur de texte brut et le contenu RTF brut correspondant du fichier copié dans l’URL de demande.

Certains traitements de texte génèrent des fichiers assez volumineux, notamment des préambules non utilisés par Scene7 Image Serving. Il est recommandé de supprimer les éléments RTF inutilisés de la chaîne avant de transmettre la chaîne aux commandes de texte.

Le codage de langue basé sur les normes UTF-8 et ISO est pris en charge dans les chaînes RTF en tant qu’alternative aux mécanismes de codage de caractères RTF standard. Cela permet aux applications d&#39;envoyer du texte non anglais au serveur sans connaissance du codage RTF.

Tous les caractères non conformes au protocole HTTP doivent être correctement placés en séquence d’échappement, si la chaîne doit être transmise via http. Seuls &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39; doivent être ignorés si la chaîne est incorporée dans le `catalog::Modifiers` champ d’un enregistrement de catalogue d’images. Les caractères de contrôle, y compris `<CR>`, `<LF>`et `<TAB>` doivent toujours être supprimés.

Les moteurs de texte Image Serving interprètent un sous-ensemble de commandes définies par la spécification RTF (Rich Text Format), version 1.6. Ce sous-ensemble est axé sur le formatage des polices et des caractères, le formatage des paragraphes simple et la prise en charge des polices et des jeux de caractères internationaux. Les éléments de formatage plus avancés, tels que les feuilles de style et les tableaux, ne sont pas pris en charge pour le moment.

La spécification RTF (Rich Text Format), telle que publiée par Microsoft, est requise lorsque vous tentez de construire manuellement des chaînes de texte codées RTF.

* [Gestion des polices](r-font-handling.md)
* [Gestion des couleurs](r-color-handling.md)
* [Copier-ajuster](r-copy-fitting.md)
* [Calques de texte](r-text-layers.md)
* [Positionnement du texte](r-text-positioning.md)
* [Caractères réservés](r-reserved-characters.md)
* [Commandes RTF et mots-clés pris en charge](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemples de codage RTF](r-rtf-encoding-examples.md)
