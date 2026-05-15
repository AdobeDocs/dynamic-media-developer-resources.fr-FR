---
description: La diffusion d’images fournit plusieurs alternatives pour le rendu du texte, accessibles avec les commandes text= et textPs= .
solution: Experience Manager
title: Formatage du texte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
TQID: 'https://experienceleague.adobe.com/OzCs0opEKfoih79LE4UuXEOJnN4Zh6iBtQNdRxCddAE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 6%

---

# Formatage du texte{#text-formatting}

La diffusion d’images fournit plusieurs alternatives pour le rendu du texte, accessibles avec les commandes text= et textPs= .

`textPs=` offre un haut niveau de similarité avec le texte rendu avec Adobe Photoshop et Illustrator. `text=` est raisonnablement compatible avec le texte rendu avec Windows Wordpad.

>[!NOTE]
>
>Outre les différences répertoriées ailleurs, `text=` produit des différences subtiles dans le texte rendu par rapport à `textPs=`. Par exemple, les soulignements n&#39;ont pas la même épaisseur ni la même position et les italiques synthétisés sont rendus sous un angle légèrement différent. Si le texte ne tient pas dans l’espace disponible, `text=` pouvez partiellement recadrer la dernière ligne, tandis que `textPs=` effectue uniquement le rendu des lignes complètes.

Toutes les commandes de texte acceptent du texte formaté basé sur un sous-ensemble de la spécification RTF (Rich Text Format). Chaque calque de texte peut spécifier une commande de texte différente.

Le tableau suivant répertorie les principales fonctionnalités disponibles pour chaque commande de texte :

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> Fonctionnalité </b> <b></th> 
   <th class="entry"> <b> text=</b> </th> 
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
   <td> <p>Déplacer le texte le long de chemins arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ajustement par copie </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Ajustement Par Copiage <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
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
   <td> <p>Texte tout en majuscules et petites majuscules </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Couleurs de diffusion d’images </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\*\iscolortable </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Plusieurs modes de lissage </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>flux de texte haut-bas/droite-gauche </p> </td> 
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
   <td> <p>Dimensionnement automatique du calque en fonction du texte </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Prise en charge du CMJN </p> </td> 
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
   <td> <p>Désactiver le retour à la ligne automatique </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mise à l’échelle automatique du texte pour l’adapter au calque (en faisant varier la résolution) </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Les chaînes compatibles RTF peuvent être assemblées manuellement ou en formatant le texte souhaité dans un éditeur de texte ou un traitement de texte capable d’enregistrer les fichiers RTF. Le fichier RTF peut ensuite être ouvert dans un éditeur de texte brut et le contenu RTF brut correspondant du fichier peut être copié dans l’URL de requête.

Certains processeurs de texte génèrent des fichiers assez volumineux, qui incluent des préambules substantiels qui ne sont pas utilisés par le service d’images Dynamic Media. Il est recommandé de supprimer les éléments RTF inutilisés de la chaîne avant de transmettre la chaîne aux commandes de texte.

Le codage de langue basé sur les normes UTF-8 et ISO est pris en charge dans les chaînes RTF comme alternative aux mécanismes de codage de caractères RTF standard. Cela permet aux applications d’envoyer du texte non anglais au serveur sans connaissance de l’encodage RTF.

Tous les caractères non conformes au protocole HTTP doivent être des caractères d’échappement si la chaîne doit être transmise par le biais du protocole HTTP. Seuls « = », «&amp; » et «% » doivent être placés dans une séquence d’échappement si la chaîne est incorporée dans le champ `catalog::Modifiers` d’un enregistrement de catalogue d’images. Les caractères de contrôle, notamment `<CR>`, `<LF>` et `<TAB>`, doivent toujours être supprimés.

Les moteurs de texte du service d’images interprètent un sous-ensemble de commandes définies par la version 1.6 de la spécification RTF (Rich Text Format). Ce sous-ensemble porte sur la mise en forme des polices/caractères, la mise en forme simple des paragraphes et la prise en charge des polices et des jeux de caractères internationaux. Les mises en forme plus avancées, telles que les feuilles de style et les tableaux, ne sont pas prises en charge pour le moment.

Vous devez connaître la spécification RTF (Rich Text Format), telle que publiée par Microsoft, lorsque vous tentez de créer manuellement des chaînes de texte codées au format RTF.

* [Gestion des polices](r-font-handling.md)
* [Gestion des couleurs](r-color-handling.md)
* [Ajustement par copie](r-copy-fitting.md)
* [Calques de texte](r-text-layers.md)
* [Positionnement du texte](r-text-positioning.md)
* [Caractères réservés](r-reserved-characters.md)
* [Commandes et mots-clés RTF pris en charge](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemples de codage RTF](r-rtf-encoding-examples.md)
