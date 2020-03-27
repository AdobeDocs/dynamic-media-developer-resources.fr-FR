---
description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement maintenus à l’aide de n’importe quel éditeur de texte.
seo-description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement maintenus à l’aide de n’importe quel éditeur de texte.
seo-title: Fichiers d’attribut de catalogue
solution: Experience Manager
title: Fichiers d’attribut de catalogue
topic: Scene7 Image Serving - Image Rendering API
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fichiers d’attribut de catalogue{#catalog-attribute-files}

Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement maintenus à l’aide de n’importe quel éditeur de texte.

Les fichiers d’attributs de catalogue se composent d’un ensemble d’enregistrements de texte, séparés par une seule `<CR>` (code ASCII `0xD`), une seule `<LF>` (code ASCII `0xA`) ou une `<CR><LF>` paire. Chaque enregistrement se compose d’un nom d’attribut et d’une ou plusieurs valeurs d’attribut séparées par des virgules :

` *`Valeurs`*= *`de nom`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valeurs</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valeurs</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nom</span> </p> </td> 
  <td class="stentry"> <p>Nom d’attribut. Peut se composer d’une ou plusieurs lettres, nombre, - et _. Non sensible à la casse. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valeur d’attribut. Ne doit pas inclure de caractères <span class="codeph"> &lt;CR&gt;</span> ou <span class="codeph"> &lt;LF&gt;</span> , sauf s’ils sont précédés d’une seule barre oblique inverse juste avant le caractère de nouvelle ligne. </p></td> 
 </tr> 
</table>

L’espace entre les jetons est facultatif.

Les enregistrements dont le nom d’attribut est inconnu sont ignorés par le serveur de plateformes.

Les noms d’attribut peuvent être composés de toute combinaison de lettres ASCII, de nombres, ainsi que de &quot;-&quot;, &quot;_&quot; et &quot;.&quot;

Si le même nom d’attribut se produit plusieurs fois dans le même fichier d’attribut, le dernier nom rencontré prévaut.

Utilisez # comme premier caractère pour marquer un enregistrement comme commentaire, ce que l&#39;analyseur ignore.
