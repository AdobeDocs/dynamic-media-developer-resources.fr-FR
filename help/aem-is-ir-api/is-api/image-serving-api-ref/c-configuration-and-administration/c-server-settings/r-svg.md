---
title: SVG
description: Les paramètres de cette section ne doivent être pris en compte que si le rendu du SVG est requis.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 2%

---

# SVG{#svg}

Les paramètres de cette section ne doivent être pris en compte que si le rendu du SVG est requis.

## SV::SvgHeapSize - Taille du tas du SVG {#section-59ab17681daa4be8b5d794713e1a504e}

Taille du tas Java pour le moteur de rendu de SVG. La valeur par défaut est &quot;200 m&quot; (200 Mo).

## PS::svgProvider.rootPaths - SVG Data Root Folders {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Emplacement des fichiers de données source du SVG. Il peut s’agir d’un ou plusieurs chemins d’accès ou chemins de fichier absolus par rapport à *[!DNL install_folder]*, séparés par des points-virgules. Généralement défini sur la même valeur que `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Taille maximale du fichier du SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Taille maximale du fichier source du SVG en kBytes. Le serveur renvoie une erreur lorsqu’une tentative de rendu d’un fichier SVG supérieur à cette limite est effectuée. La valeur par défaut est de 1 024 Ko.

## IS::SvgMAxRenderRgnPixels - Limite de taille de l’image de sortie SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Cela limite la taille des images que SVGRender peut produire. Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si une opération de rendu dépasse la limite de taille. La valeur par défaut est de 4.

## PS::svgProvider.port - [!DNL Platform Server] Port d’écoute {#section-f7e42a96c2dd4523b46f0557c239e659}

Port utilisé pour SvgRender pour obtenir des images de [!DNL Platform Server] à incorporer dans les rendus de SVG.

Important : Pour que le composant SVGRender fonctionne correctement, cette option de configuration doit être définie sur la même valeur que `TC::PsPort`.

## PS::svgProvider.fontRoot - Dossier des fichiers de polices du SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Indique l’emplacement où le SvgRender trouve les fichiers de polices nécessaires au rendu du texte du SVG ; généralement l’un des chemins spécifiés dans `IS::RootPaths`. La valeur par défaut est [!DNL *[!DNL install_folder]*/images].

## SVG ::SVGRender.port, IS::SVGTcpPort - Port des communications du SVG {#section-608687123aa644b7b58fe42385d71b79}

Configure le port sur lequel le serveur d’images et le composant SVGRender communiquent.

>[!NOTE]
>
>Pour que le composant SVGRender fonctionne correctement, le même numéro de port doit être spécifié pour `SVG::SVGRender.port` et `IS::SVGTcpPort`.
