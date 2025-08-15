---
title: Personnalisation de la visionneuse panoramique
description: Toute la personnalisation visuelle et la plupart des personnalisations de comportement pour la visionneuse panoramique se font en créant un CSS personnalisé.
keywords: sensible
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Personnalisation de la visionneuse Video360{#customizing-video-viewer}

Toute la personnalisation visuelle et la plupart des personnalisations de comportement se font en créant un CSS personnalisé.

Le flux de travail suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier dans un emplacement différent, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7viewers_root>/html5/PanoramicViewer.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que le fichier par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre façon de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lors de la création d’une feuille CSS personnalisée, n’oubliez pas que la visionneuse attribue une `.s7panoramicviewer` classe à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec `style=` la commande, utilisez `.s7panoramicviewer` la classe comme classe parent dans le sélecteur de descendants de vos règles CSS. Si vous utilisez des styles incorporés sur la page Web, qualifiez également ce sélecteur avec un ID de l’élément DOM conteneur comme suit :

`#<containerId>.s7panoramicviewer.`


## Notes générales de style et conseils {#section-95855dccbbc444e79970f1aaa3260b7b}

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non à l’emplacement de la page HTML de la visionneuse. Tenez-en compte lorsque vous copiez le CSS par défaut vers un emplacement différent : il peut être nécessaire de copier également les ressources par défaut ou de mettre à jour les chemins dans le CSS personnalisé.
* Vous pouvez utiliser différents formats pour la valeur colorimétrique pris en charge par CSS. Si de la transparence est nécessaire, `rgba(R,G,B,A)` le format est suggéré. Sinon, la transparence n’est pas requise `#RRGGBB` peut être utilisée.

Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle n’est pas prise en charge pour définir le style des éléments de `!IMPORTANT` la visionneuse. En particulier, `!IMPORTANT` la règle ne doit pas être utilisée pour remplacer un style par défaut ou d’exécution fourni par la visionneuse ou le Kit de développement logiciel (SDK) de la visionneuse, car cela peut affecter le comportement correct des composants. Au lieu de cela, des sélecteurs CSS avec la spécificité appropriée doivent être utilisés pour définir les propriétés CSS documentées dans ce guide de référence.

## CSS de visionneuse panoramique {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Zone** principale de la visionneuse
La zone de vue principale est la zone occupée par l’image panoramique.  En règle générale, elle est configurée pour s’adapter à l’écran disponible du périphérique lorsqu’aucune taille n’est spécifiée.

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS :`.s7panoramicviewer`

Les propriétés CSS applicables sont les suivantes :

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la largeur de la visionneuse ; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la hauteur de la visionneuse ; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple:
Configuration d’une visionneuse d’une taille de 1024 x 512 pixels.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Vue** panoramique
La vue principale se compose de l’image panoramique.

L’aspect de la vue principale est contrôlé par le sélecteur de classe CSS :`.s7panoramicviewer .s7panoramicview`

Les propriétés CSS applicables sont les suivantes :
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Couleur d’arrière-plan de la vue principale ; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple:
Pour rendre la vue principale transparente :

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
