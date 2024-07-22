---
title: Personnalisation de la visionneuse panoramique
description: Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse panoramique sont effectuées par la création d’une page CSS personnalisée.
keywords: responsive
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

Toutes les personnalisations visuelles et la plupart des personnalisations du comportement sont effectuées en créant une page CSS personnalisée.

Le workflow suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser, et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7viewers_root>/html5/PanoramicViewer.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que celles par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement, car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que la visionneuse affecte la classe `.s7panoramicviewer` à son élément DOM de conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez la classe `.s7panoramicviewer` comme classe parente dans le sélecteur descendant pour vos règles CSS. Si vous effectuez des styles intégrés sur la page web, qualifiez en outre ce sélecteur avec un identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7panoramicviewer.`


## Notes et conseils généraux sur le style {#section-95855dccbbc444e79970f1aaa3260b7b}

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page d’HTML de la visionneuse. Tenez compte de cela lors de la copie du CSS par défaut vers un autre emplacement : il peut être nécessaire de copier les ressources par défaut également ou de mettre à jour les chemins d’accès dans le CSS personnalisé.
* Vous pouvez utiliser différents formats pour la valeur de couleur prise en charge par CSS. Si la transparence est nécessaire, le format `rgba(R,G,B,A)` est suggéré. Sinon, la transparence n&#39;est pas requise `#RRGGBB` peut être utilisée.

Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour appliquer un style aux éléments de la visionneuse. En particulier, la règle `!IMPORTANT` ne doit pas être utilisée pour remplacer les styles par défaut ou d’exécution fournis par la visionneuse ou le SDK de la visionneuse, car ils peuvent affecter le comportement correct des composants. Au lieu de cela, les sélecteurs CSS avec une précision appropriée doivent être utilisés pour définir les propriétés CSS documentées dans ce guide de référence.

## CSS de visionneuse panoramique {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Zone de visionneuse principale**
La zone de vue principale est la zone occupée par l&#39;image panoramique.  Il est généralement défini pour s’adapter à l’écran de l’appareil disponible lorsqu’aucune taille n’est spécifiée.

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS :
`.s7panoramicviewer`

Les propriétés CSS applicables incluent :

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la largeur de la visionneuse ; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la hauteur de la visionneuse ; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple :
Pour configurer une visionneuse d’une taille de 1 024 x 512 pixels.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Vue panoramique**
La vue principale est composée de l’image panoramique.

L’aspect de la vue principale est contrôlé à l’aide du sélecteur de classe CSS :
`.s7panoramicviewer .s7panoramicview`

Les propriétés CSS applicables incluent :
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> : couleur d’arrière-plan de la vue principale ; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple :
Pour rendre l’affichage principal transparent :

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
