---
title: SVG
description: Les paramètres de cette section doivent être pris en compte uniquement si le rendu SVG est requis.
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

Les paramètres de cette section doivent être pris en compte uniquement si le rendu SVG est requis.

## SV::SvgHeapSize - Taille du tas SVG {#section-59ab17681daa4be8b5d794713e1a504e}

Taille du tas Java pour le rendu SVG. La valeur par défaut est « 200m » (200 Mo).

## PS::svgProvider.rootPaths - Dossiers racine de données SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Emplacement des fichiers de données sources SVG. Il peut s’agir d’un ou plusieurs chemins d’accès absolus aux fichiers ou de chemins d’accès relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Défini généralement sur la même valeur que `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Taille maximale du fichier SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Taille maximale du fichier source SVG en kOctets. Le serveur renvoie une erreur lorsqu’une tentative est effectuée pour effectuer le rendu d’un fichier SVG dont la taille est supérieure à cette limite. La valeur par défaut est de 1 024 Ko.

## IS::SvgMAxRenderRgnPixels - Limite de taille d’image de sortie SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Il limite la taille des images que SVGRender peut produire. Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si une opération de rendu dépasse la taille limite. La valeur par défaut est de 4.

## PS::svgProvider.port - Port d&#39;écoute [!DNL Platform Server] {#section-f7e42a96c2dd4523b46f0557c239e659}

Port utilisé par SvgRender pour obtenir des images du [!DNL Platform Server] à incorporer dans des rendus SVG.

Important Pour le bon fonctionnement du composant SVGRender, cette option de configuration doit être définie sur la même valeur que `TC::PsPort`.

## PS::svgProvider.fontRoot - Dossier Fichiers de polices SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Indique l’emplacement où SvgRender trouve les fichiers de polices nécessaires au rendu du texte SVG. Il s’agit généralement de l’un des chemins spécifiés dans `IS::RootPaths`. La valeur par défaut est [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Port de communication SVG {#section-608687123aa644b7b58fe42385d71b79}

Configure le port sur lequel le serveur d’images et le composant SVGRender communiquent.

>[!NOTE]
>
>Pour le bon fonctionnement du composant SVGRender, le même numéro de port doit être spécifié pour `SVG::SVGRender.port` et `IS::SVGTcpPort`.
