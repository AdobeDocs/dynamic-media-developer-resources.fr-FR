---
description: Objet ou conteneur dans la hiérarchie de dossiers.
solution: Experience Manager
title: Atout
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---

# [!DNL Asset]{#asset}

Objet ou conteneur dans la hiérarchie de dossiers.

Syntaxe

## Paramètres {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL acoInfo]</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL animatedGifInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :GifInfo animé</span> </td> 
   <td colname="col3"> Détails d’un fichier GIF animé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Gestion des ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetSetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cabinetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :CabinetInfo</span> </td> 
   <td colname="col3"> Propriétés d’un type de ressource d’armoire. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL created]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :dateTime</span> </td> 
   <td colname="col3"> Date et heure auxquelles la ressource a été transférée. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL createUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Adresse électronique de l’utilisateur qui a créé la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cssInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :CssInfo</span> </td> 
   <td colname="col3"> Détails d’un fichier CSS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cuePointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL excelInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3">Renvoie le nom de fichier virtuel. Le chemin d’accès complet au fichier virtuel est <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL flashInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Dossier contenant une ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folderHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Gérez le dossier parent de la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fontInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type :infos de police</span> </td> 
   <td colname="col3"> Propriétés d’un fichier de polices. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL iccProfileInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :IccProfileInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource de profil ICC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL illustratorInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :InfoImageInfo</span> </td> 
   <td colname="col3"> Propriétés d’un fichier image. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL inDesignInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL ipsImageUrl]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> URL relative représentant une miniature de la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL javascriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :JavascriptInfo</span> </td> 
   <td colname="col3"> Détails d’un fichier JavaScript. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModified]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :dateTime</span> </td> 
   <td colname="col3"> Date et heure de la dernière modification de la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModifyUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Adresse électronique de l’utilisateur qui a modifié la ressource en dernier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL layerViewInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :LayerViewInfo</span> </td> 
   <td colname="col3"> Propriétés d’un fichier de vue de calque. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masterVideoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL metadataArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :MetadataArray</span> </td> 
   <td colname="col3"> Tableau des valeurs de métadonnées associées à la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL name]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Nom de la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfSettingsInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PdfSettingsInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource de paramètres PDF. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL permissions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL postScriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL powerPointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL premiereExpressInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL projects]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Liste des noms de projets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL psdInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> Définit un indicateur pour indiquer si une ressource doit être publiée ou non. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL renderSceneInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :RenderSceneInfo</span> </td> 
   <td colname="col3"> Propriétés d’un fichier de scène de rendu. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL rtfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL subType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3">Sous-type de ressource générique prenant en charge les valeurs de sous-type (par exemple, <span class="codeph"> AssetSet</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL svgInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :SvgInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource SVG. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL swcInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :SwcInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource SWC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL templateInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :TemplateInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource de modèle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL trashState]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Indique si un fichier est dans la corbeille ou actif (voir « État de la corbeille » pour les valeurs). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL type]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3">Type de ressource. Voir <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> Types de</a> ressources pour connaître les valeurs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoCaptionInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>Propriétés d’un fichier de sous-titrage vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> <p>Propriétés d’une ressource vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerPresetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ViewerPresetInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource de paramètre prédéfini de visionneuse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerSwfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ViewerSwfInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource SWf de visionneuse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL vignetteInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VignetteInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource de vignette. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL watermarkInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :WatermarkInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource de filigrane. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL windowCoveringInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :WindowCoveringInfo</span> </td> 
   <td colname="col3"> Propriétés d’un actif de garniture de fenêtre. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL wordInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL xmlInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :XmlInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource XML. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Infos xsl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :XslInfo</span> </td> 
   <td colname="col3"> Propriétés d’une ressource XSL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Informations</span> sur la compression </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
