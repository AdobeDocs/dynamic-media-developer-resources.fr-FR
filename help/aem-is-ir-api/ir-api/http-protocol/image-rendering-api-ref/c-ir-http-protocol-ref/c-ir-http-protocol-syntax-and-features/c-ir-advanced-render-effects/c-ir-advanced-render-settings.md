---
description: L’outil de création de vignettes (qui fait partie du pack de création d’images Dynamic Media) fournit des mécanismes permettant de contrôler les aspects de bas niveau du moteur de rendu de vignette.
solution: Experience Manager
title: Paramètres de rendu avancés
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 25%

---


# Paramètres de rendu avancés{#advanced-render-settings}

L’outil de création de vignettes (qui fait partie du pack de création d’images Dynamic Media) fournit des mécanismes permettant de contrôler les aspects de bas niveau du moteur de rendu de vignette.

>[!NOTE]
>
>Les paramètres de rendu sont une fonctionnalité avancée de rendu d’image et de création d’images. Contactez le support technique de l’Adobe ou votre représentant-conseil Adobe pour obtenir de la formation, des consultations ou les deux, sur l’utilisation des paramètres de rendu.

Ces paramètres sont contrôlés de manière interactive dans la création d’images. Il est possible d’appliquer les mêmes paramètres dans le rendu d’image à l’aide de la commande `rs=` (ou avec la valeur `catalog::RenderSettings`). Ce mécanisme permet de sélectionner différentes options d’accentuation pour chaque matériau et de modifier le comportement des algorithmes de rendu de l’éclairage, comme la variation de la saturation des tons clairs ou le contraste des tons foncés.

## Valeurs de paramètre de rendu avancé (rs=) {#section-d9e7f341ebd44f07a4e90f1f5910726b}

<table id="table_1517FC39C7344EBB9F17BE20415DB057"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Code </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Valeur minimale </p> </th> 
   <th colname="col4" class="entry"> <p>Valeur maximale </p> </th> 
   <th colname="col5" class="entry"> <p>Remarques </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col2"> <p>Render Effects/Alternate Shader remplace le paramètre de la vignette. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>A0=Effets de rendu </p> <p>A1=Autre Shader </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U </p> </td> 
   <td colname="col2"> <p>USM (nonSharp Mask). </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>2 </p> </td> 
   <td colname="col5"> <p>Pour utiliser USM, U doit être &gt; 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>W </p> </td> 
   <td colname="col2"> <p>Montant USM (%). </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>500 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V </p> </td> 
   <td colname="col2"> <p>Rayon USM (pixels). </p> </td> 
   <td colname="col3"> <p>3 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>X </p> </td> 
   <td colname="col2"> <p>Seuil USM (niveaux). </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q </p> </td> 
   <td colname="col2"> <p>Mode de redimensionnement. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_87184BB93E7F46D59BA1AAAFA8455512"> 
      <li id="li_E7711C3678ED4DE09E710F7C430CEF42">Le voisin le plus proche </li> 
      <li id="li_CAE975B91C604DA0AA493F700AEBE199">Bi-Linéaire </li> 
      <li id="li_24E5A40B8A3F4C808A68686C27647CD5">Bicubique </li> 
      <li id="li_42ACFCE65B4843ACAFA6A52255364642">Suréchantillonnage (valeur par défaut) </li> 
      <li id="li_34EC85C4D15145DF80F7D3DB7B6244D3">Fenêtre Lanczos </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>R </p> </td> 
   <td colname="col2"> <p>Mode de rééchantillonnage. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_FD4A9D73C32F47C3BF13776BB4D2818D"> 
      <li id="li_F08AD1D093D74059B60302374B472B52">Par défaut </li> 
      <li id="li_FD4C859D975B44399475D4D93D6B05AB">Le voisin le plus proche </li> 
      <li id="li_CA93566F5D4F4D3CAA1D0816562A3851">Bi-Linéaire </li> 
      <li id="li_D334ACF969E749A89A464B21C96CE8A6">Suréchantillonnage </li> 
      <li id="li_FAC72C36FF4A418F8A5B05F3B4E7C5D8">Adaptatif </li> 
      <li id="li_6E9D81045A0C4804A4D35D9B239F6486">Echantillon de Poisson </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>Suréchantillonnage : Aléatoire. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>200 </p> </td> 
   <td colname="col5"> <p>Valeur par défaut : 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>Suréchantillonnage : Taux aléatoire. </p> </td> 
   <td colname="col3"> <p>3 </p> </td> 
   <td colname="col4"> <p>20 </p> </td> 
   <td colname="col5"> <p>Valeur par défaut : 5. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>M </p> </td> 
   <td colname="col2"> <p>Redimensionnement adaptatif : Profondeur. </p> </td> 
   <td colname="col3"> <p>4 </p> </td> 
   <td colname="col4"> <p>8 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>N </p> </td> 
   <td colname="col2"> <p>Redimensionnement adaptatif : Largeur. </p> </td> 
   <td colname="col3"> <p>2 </p> </td> 
   <td colname="col4"> <p>10 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>P </p> </td> 
   <td colname="col2"> <p>Poisson : Exemples/pixels. </p> </td> 
   <td colname="col3"> <p>3 </p> </td> 
   <td colname="col4"> <p>4 </p> </td> 
   <td colname="col5"> <p>Valeur par défaut : 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>O </p> </td> 
   <td colname="col2"> <p>Poisson : Utiliser la bascule. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>3 </p> </td> 
   <td colname="col5"> <p>Valeur par défaut : 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Effets de rendu (shader plus ancien)</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I </p> </td> 
   <td colname="col2"> <p>Faits saillants. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>J </p> </td> 
   <td colname="col2"> <p>Met en évidence la saturation. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>50 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H </p> </td> 
   <td colname="col2"> <p>Des ombres pour des matériaux clairs. </p> </td> 
   <td colname="col3"> <p>50 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>K </p> </td> 
   <td colname="col2"> <p>Saturation de l'ombre. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>400 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>Force de l'extrapolation basée sur la brillance. </p> </td> 
   <td colname="col3"> <p>100 </p> </td> 
   <td colname="col4"> <p>600 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0 </p> </td> 
   <td colname="col2"> <p>Compensation de la luminosité (case à cocher) </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p>La valeur par défaut est on (blank) et désélectionnée = F100G0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Autre shader</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Z </p> </td> 
   <td colname="col2"> <p>Contraste de base. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>Valeur par défaut : 50. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>a </p> </td> 
   <td colname="col2"> <p>Compensation de la luminosité. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : a36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>b </p> </td> 
   <td colname="col2"> <p>Réglage de la saturation. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : b36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>c </p> </td> 
   <td colname="col2"> <p>Réglage des ombres. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : c36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>d </p> </td> 
   <td colname="col2"> <p>Met en évidence l'ajustement. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : d36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>e </p> </td> 
   <td colname="col2"> <p>Faits saillants spectaculaires. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : e36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>xx </p> </td> 
   <td colname="col2"> <p>Forme. </p> </td> 
   <td colname="col3"> <p>-100 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>Voir "xx" dans les valeurs ci-dessus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> <p>Réglage de l'éclairage. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : k64.138.175.60.xx.133.242 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>u &amp; s </p> </td> 
   <td colname="col2"> <p>Changement de teinte de l'ombre. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : u8.1.2.3.4.5.6.7.8.s8.1.2.3.4.5.6.7.8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>v &amp; t </p> </td> 
   <td colname="col2"> <p>Mettez en surbrillance le décalage de teinte. </p> </td> 
   <td colname="col3"> <p>01 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format différent : v8.1.2.3.4.5.6.7.8.t8.1.2.3.4.5.6.7.8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>w </p> </td> 
   <td colname="col2"> <p>Réglage de la saturation. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>g </p> </td> 
   <td colname="col2"> <p>Augmentation de faible saturation. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples de paramètres de rendu avancé {#section-56528569eae44ecd997a289b211ff256}

<table id="table_062DCF66ACCC4A6997E3CA951C0A12B8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Configuration de la composition </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>H60I30J10K200L400U1V10W100X0 </p> </td> 
   <td colname="col2"> <p>Valeurs par défaut dans la création d’images. 
     <ul id="ul_AA7CF1A3E6984B318265BBE8FFFBB4EE">
      <li> USM1
      <li id="li_8EC075956E2E4D5A91355122DC9BC938">H60 = Ombres pour les matériaux lumineux (50-100). </li> 
      <li id="li_F760B65E057146A7B56673D6B1A9A304">I30 = Points saillants (0-100). </li> 
      <li id="li_376C275FDB3548958C09BD266C77318F">J10 = Met en surbrillance la saturation (0-50). </li> 
      <li id="li_FE26429972F544869CDFE2DD61F39CC5">K200 = saturation des ombres (0-400). </li> 
      <li id="li_FB6BAA708427428AA4A3AC2E5D3B9932">L400 = résistance à l'extrapolation basée sur la brillance (100-600). </li> 
      <li id="li_6B2EEEE7F0D54E078462AAFC4E4FAB42">U1 = USM (Accentuation) (0-2). </li> 
      <li id="li_7CD4E3662A6C48F9B5895D133D28BA2A">V10 = rayon USM (1-100 pixels). </li> 
      <li id="li_949B6DB4959B46A892787CD5B3AD7485">W100 = montant USM (1 à 500 %). </li> 
      <li id="li_F39D3834D4A2478D993E5E9C9B434CFE">X0 = seuil USM (0 à 255 niveaux). </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C6E6DD90ECAB4D2B9284A25A29923DC6"> 
      <li id="li_7B7A8C43BCEB4CB58C7074974CAB0419">USM1 </li> 
      <li id="li_A003B68023424DCABBF3A2CAF98C39A4">La compensation maximale et de luminosité est activée. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_AAEC098CED1C436E933B1C1B88DFB659"> 
      <li id="li_0CC34CDD796E4DFD802824FF21DB021B">USM1 </li> 
      <li id="li_E36886FB1D00444CBA19D7245E89B292">La compensation maximale et de luminosité est désactivée. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H100I100J50K400L600U2V100W500X255 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6BB668C6C055493DAAA38F4D3B9C20A7"> 
      <li id="li_D8BAFB41CF4C4B3FAD6F89AF5D7F223A">USM2 </li> 
      <li id="li_DA685F4DE4BA427BA7BE241A75C96152">La compensation maximale et de luminosité est désactivée. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H80I70J40L300U1V8W80X5 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7C374842312E4AD0B62692BBCE6743A8"> 
      <li id="li_CC730580B54741FBBBFF507DE0FE1F15">H80 = montant USM </li> 
      <li id="li_C2801B2C093444AC9401793BC571EC27">I70 = Points saillants </li> 
      <li id="li_518C6A690EC34614B0806A0C6BC535FF">J40 = Saturation des surbrillances </li> 
      <li id="li_F280CF29D1E341D9AC9C0C16C2DEA1E6">L300 = résistance à l'extrapolation basée sur la brillance </li> 
      <li id="li_3F589F109AC94280911BD535C49E42E4">U1 = USM </li> 
      <li id="li_113FEC9B37D54511BAB3FEAC7C271858">V8 = rayon USM </li> 
      <li id="li_E1BA7406A76B476EB1A89D6EDD87930C">W80 = Ombres pour les matériaux brillants </li> 
      <li id="li_AAD479EF6A7F43B98A8C147FCD684ECA">X5 = seuil USM </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q5R3S11T103U1V6W120X5Z80b.188.88.75.37 </p> </td> 
   <td colname="col2"> <p>Autre Shader avec accentuation : </p> <p> 
     <ul id="ul_93AD53BB37EA47F6A3CEE424D3AAE18C"> 
      <li id="li_9EF1DF4167164721882E4842C2E0B20C">USM1 </li> 
      <li id="li_7B5D8B7BB5544E7FA4AD702EE281086B">Montant USM (120) </li> 
      <li id="li_B3BE096BB0654A2DBADDD6832E499F2A">Rayon USM (0,6) </li> 
      <li id="li_793DAB145CE7469ABC1182BCBD324657">Seuil USM (5) </li> 
      <li id="li_B1954FEBE2084726828D64E8165DA4DA">Redimensionnement (Lanczos) </li> 
      <li id="li_E5ED76998C0543D8A3F9AD178CFD3C2C">Rééchantillonnage (échantillonnage superflu, aléatoire=moitié, rate=half)) </li> 
      <li id="li_CCEE53544E7D48858398BF3168F1E87D">Contraste (plus fort) </li> 
      <li id="li_EB0D25C095FB4D5798AC031AB759849B">Réglage de la saturation (premier sommet au milieu, deuxième sommet le long du bord, troisième sommet au milieu inférieur) </li> 
      <li id="li_5C2304DA4A4D4799AE5DCCCB1E2ECBB3">Accentuation (3/4 vers la droite) </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- RB: I don't know why this is in here; it was added by someone else: 
Alternate Shader Rendering (default on) checkbox provides a more precise Advanced Shader diffuse rendering pipeline. For a number of effects it also provides an alternate Advanced Shader rendering pipeline. Note that the underlying OpenGL hardware must provide support for the Advanced (Per-Pixel) GLSL Shaders for this option to be vailable; else this checkbox is automatically disabled. -->

<!-- RB: I don't know why this is in here; it was added by someone else:
It should probably also go into the different renders - Render Effects and Alternate Shader - or link to descriptions of each. -->
