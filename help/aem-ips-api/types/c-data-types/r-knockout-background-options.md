---
title: KnockoutBackgroundOptions
description: Masquer (masquer) l’arrière-plan des images sélectionnées. Ce type de données permet de les superposer dans d’autres calques avec une transparence en dehors de l’objet. Paramètre facultatif désactivé par défaut.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 5%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

Masquer (masquer) l’arrière-plan des images sélectionnées. Ce type de données permet de les superposer dans d’autres calques avec une transparence en dehors de l’image objet.

Ce type de données est facultatif et désactivé par défaut.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## Paramètres {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>Si vous configurez `KnockoutBackgroundOptions` Dans Adobe Experience Manager, utilisez plutôt les paramètres suivants :
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>Par exemple: `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Sélectionne le coin que vous souhaitez utiliser. <span class="codeph"> corner</span> accepte ces valeurs : 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> BottomLeft</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> BottomRight</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolérance</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Paramètre facultatif qui supprime l’espace blanc des bords de l’image en fonction de la transparence. Accepte une plage de valeurs comprise entre 0,0 et 1,0. Spécifiez : 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 pour faire correspondre exactement les couleurs. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 pour activer le plus grand nombre de différences de couleurs. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Contrôler la transparence des pixels à l’emplacement spécifié par la variable <span class="codeph"><span class="varname"> corner</span></span> . Le <span class="codeph"> fillMethod</span> accepte ces valeurs : </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: Rend transparents tous les pixels dans le coin spécifié. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: Rend transparents tous les pixels correspondants, quel que soit l’emplacement. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## Utilisé par {#section-28c43baafe85434a9ee9e303ed10569a}

Le `KnockoutBackgroundOptions` type utilisé par :

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
