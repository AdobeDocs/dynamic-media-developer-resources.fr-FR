---
title: KnockoutBackgroundOptions
description: Masque (masquage) l’arrière-plan des images sélectionnées. Ce type de données vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image de l’objet. Paramètre facultatif qui est désactivé par défaut.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
TQID: 'https://experienceleague.adobe.com/8DZwQo12bsutVbNdfz2XtpX4sO4pTbbjdtYqrn00-1w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 2%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

Masque (masquage) l’arrière-plan des images sélectionnées. Ce type de données vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image de l’objet.

Ce type de données est facultatif et désactivé par défaut.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## Paramètres {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>Si vous configurez `KnockoutBackgroundOptions` dans Adobe Experience Manager, utilisez plutôt les paramètres suivants :
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>Par exemple : `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> coin </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Sélectionne le coin avec lequel vous souhaitez travailler. <span class="codeph"> corner </span> accepte les valeurs suivantes : <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> En haut à gauche</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> En bas à gauche</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> En bas à droite</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolérance</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Paramètre facultatif qui supprime les espaces blancs des bords d’image en fonction de la transparence. Accepte une plage de valeurs comprise entre 0,0 et 1,0. Spécifiez les éléments suivants : <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 pour correspondre exactement aux couleurs. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 pour activer le plus de différences de couleurs. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Contrôle la transparence des pixels à l’emplacement spécifié par la variable <span class="codeph"><span class="varname"> corner</span></span>. La méthode <span class="codeph"> fillMethod</span> accepte les valeurs suivantes : </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill </span> : rend transparents tous les pixels du coin spécifié. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel </span> : rend transparents tous les pixels correspondants, quel que soit l’emplacement. </li> 
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

Le type de `KnockoutBackgroundOptions` est utilisé par :

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

