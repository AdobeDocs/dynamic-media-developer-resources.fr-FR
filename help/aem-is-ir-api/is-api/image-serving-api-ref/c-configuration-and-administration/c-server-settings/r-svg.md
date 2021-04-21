---
description: Les paramètres de cette section doivent être pris en compte uniquement si le rendu SVG est requis.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---


# SVG{#svg}

Les paramètres de cette section doivent être pris en compte uniquement si le rendu SVG est requis.

## SV::SvgHeapSize - Taille du tas SVG {#section-59ab17681daa4be8b5d794713e1a504e}

Taille du tas Java du rendu SVG. La valeur par défaut est 200 m (200 Mo).

## PS::svgProvider.rootPaths - Dossiers racine de données SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Emplacement des fichiers de données source SVG. Il peut s’agir d’un ou plusieurs chemins d’accès ou chemins de fichier absolus relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Généralement définie sur la même valeur que `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Taille maximale du fichier SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Taille maximale du fichier source SVG en kBytes. Le serveur renvoie une erreur lorsqu’une tentative de rendu d’un fichier SVG supérieur à cette limite est effectuée. La valeur par défaut est de 1 024 octets.

## IS::SvgMAxRenderRgnPixels - Taille d’image de sortie SVG limitée {#section-5be1fd9639424d878a5ffd11736d3920}

Limite la taille des images que SVGRender peut produire. Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si une opération de rendu dépasse la limite de taille. Par défaut : 4.

## PS::svgProvider.port - Port d’écoute du serveur de plateformes {#section-f7e42a96c2dd4523b46f0557c239e659}

Port utilisé pour SvgRender pour obtenir des images du serveur de plateformes à incorporer dans les rendus SVG.

Important Pour que le composant SVGRender fonctionne correctement, cette option de configuration doit être définie sur la même valeur que `TC::PsPort`.

## PS::svgProvider.fontRoot - Dossier Fichiers de polices SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Indique où SvgRender trouvera les fichiers de polices nécessaires au rendu du texte SVG ; généralement l&#39;un des chemins spécifiés dans `IS::RootPaths`. La valeur par défaut est [ ! DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Port de communications SVG {#section-608687123aa644b7b58fe42385d71b79}

Configure le port sur lequel le serveur d’images et le composant SVGRender communiquent.

>[!NOTE]
>
>Pour que le composant SVGRender fonctionne correctement, le même numéro de port doit être spécifié pour `SVG::SVGRender.port` et `IS::SVGTcpPort`.

