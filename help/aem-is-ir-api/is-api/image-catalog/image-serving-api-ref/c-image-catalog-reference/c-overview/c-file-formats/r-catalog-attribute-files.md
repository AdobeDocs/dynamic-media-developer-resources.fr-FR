---
description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement conservés dans n’importe quel éditeur de texte.
solution: Experience Manager
title: Fichiers d’attributs du catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Fichiers d’attributs du catalogue{#catalog-attribute-files}

Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent avoir un suffixe de fichier .ini. Ils peuvent être facilement conservés dans n’importe quel éditeur de texte.

Les fichiers d’attributs du catalogue se composent d’un ensemble d’enregistrements de texte, séparés par une seule `<CR>` (code ASCII `0xD`), une seule `<LF>` (code ASCII `0xA`) ou une paire `<CR><LF>`. Chaque enregistrement se compose d’un nom d’attribut et d’une ou plusieurs valeurs d’attribut séparées par des virgules :

`*``*= *`namevalues`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valeurs</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valeurs</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nom d’attribut. Peut comprendre une ou plusieurs lettres, nombre, - et _. Non sensible à la casse. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valeur d’attribut. Ne doit pas inclure de caractères <span class="codeph"> &lt;CR&gt;</span> ou <span class="codeph"> &lt;LF&gt;</span>, à moins qu’une seule barre oblique inverse ne s’affiche juste avant le caractère de nouvelle ligne. </p></td> 
 </tr> 
</table>

L’espace entre les jetons est facultatif.

Les enregistrements avec des noms d&#39;attribut inconnus sont ignorés par le serveur de plateformes.

Les noms d&#39;attribut peuvent être composés de toute combinaison de lettres ASCII, de nombres, ainsi que de &quot;-&quot;, &quot;_&quot; et &quot;.&quot;.

Si le même nom d&#39;attribut apparaît plusieurs fois dans le même fichier d&#39;attribut, la dernière occurrence prévaut.

Utilisez # comme premier caractère pour marquer un enregistrement comme commentaire, ce que l&#39;analyseur ignore.
