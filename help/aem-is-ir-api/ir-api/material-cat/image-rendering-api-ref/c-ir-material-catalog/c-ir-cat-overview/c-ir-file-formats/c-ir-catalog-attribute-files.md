---
description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement conservés dans n’importe quel éditeur de texte.
seo-description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement conservés dans n’importe quel éditeur de texte.
seo-title: Fichiers d’attributs du catalogue
solution: Experience Manager
title: Fichiers d’attributs du catalogue
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# Fichiers d’attributs du catalogue{#catalog-attribute-files}

Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement conservés dans n’importe quel éditeur de texte.

Les fichiers d’attributs du catalogue se composent d’un ensemble d’enregistrements de texte, séparés par une seule `<CR>` (code ASCII 0xD), une seule `<LF>` (code ASCII 0xA) ou une paire `<CR><LF>`. Chaque enregistrement se compose d’un nom d’attribut et d’une ou plusieurs valeurs d’attribut séparées par des virgules :

` *``*= *``*&#42;[, *`namevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom d'attribut ; peut comprendre une ou plusieurs lettres, nombre, "-" et "_"; non sensible à la casse. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur d'attribut ; ne doit pas inclure de caractères <span class="codeph"> &lt;CR&gt; </span>, ou <span class="codeph"> &lt;LF&gt; </span>, sauf si une seule barre oblique inverse s’affiche juste avant le caractère de nouvelle ligne. </p> </td> 
 </tr> 
</table>

* L’espace entre les jetons est facultatif.
* Les enregistrements avec des noms d&#39;attribut inconnus sont ignorés par le serveur de plateformes.
* Les noms d&#39;attribut peuvent être composés de toute combinaison de lettres ASCII, de chiffres, de &quot;-&quot;, &quot;_&quot; et &quot;.&quot;
* Si le même nom d&#39;attribut apparaît plusieurs fois dans le même fichier d&#39;attribut, la dernière occurrence prévaut.
* Utilisez &quot;#&quot; comme premier caractère pour marquer un enregistrement comme commentaire que l&#39;analyseur ignore.

