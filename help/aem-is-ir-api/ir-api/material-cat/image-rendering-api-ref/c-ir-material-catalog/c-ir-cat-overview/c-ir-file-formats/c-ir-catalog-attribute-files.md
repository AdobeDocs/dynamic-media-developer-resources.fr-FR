---
title: Fichiers d’attributs de catalogue
description: Les fichiers d’attributs de catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Ils peuvent être facilement conservés à l’aide de n’importe quel éditeur de texte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Fichiers d’attributs de catalogue{#catalog-attribute-files}

Les fichiers d’attributs de catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier `.ini`. Ils peuvent être facilement conservés à l’aide de n’importe quel éditeur de texte.

Les fichiers d’attributs de catalogue se composent d’un ensemble d’enregistrements texte, séparés par une seule `<CR>` (code ASCII 0xD), une seule `<LF>` (code ASCII 0xA) ou une paire de `<CR><LF>`. Chaque enregistrement se compose d’un nom d’attribut et d’une ou de plusieurs valeurs d’attribut séparées par des virgules :

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de l’attribut ; peut se composer d’une ou de plusieurs lettres, d’un nombre, d’un - (trait d’union) et d’un _ (trait de soulignement) ; non sensible à la casse.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> valeur <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>La valeur d’attribut ne doit pas inclure <span class="codeph"> &lt;CR&gt; </span> ni <span class="codeph"> &lt;LF&gt; caractères </span>, sauf s’ils sont précédés d’une barre oblique inverse juste avant le caractère de nouvelle ligne. </p> </td> 
 </tr> 
</table>

* L’espace blanc entre les jetons est facultatif.
* Le [!DNL Platform Server] ignore les enregistrements dont les noms d’attribut sont inconnus.
* Les noms d’attribut peuvent consister en n’importe quelle combinaison de lettres ASCII, de chiffres, de caractères `-`, `_` et `.`.
* Si le même nom d’attribut apparaît plusieurs fois dans le même fichier d’attribut, le dernier événement rencontré prévaut.
* Utilisez `#` comme premier caractère pour marquer un enregistrement comme commentaire que l’analyseur ignore.
