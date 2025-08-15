---
title: Configuration requise pour Dynamic Media visionneuses HTML5
description: Configuration requise pour Dynamic Media visionneuses HTML5.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 2%

---

# Dynamic Media configuration système requise pour les visionneuses HTML5{#system-requirements}

Configuration requise pour Dynamic Media visionneuses HTML5.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Matériel et logiciels du serveur {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 ou version ultérieure.
* Les visionneuses HTML5 nécessitent le SDK JavaScript les bibliothèques côté serveur 3.11.5 ou version ultérieure.
* *Envoyer un courrier électronique à un ami* Les fonctions sociales nécessitent la version S7OnDemand 5.0.9 ou ultérieure.
* Visionneuse de catalogue électronique – [La prise en charge des fenêtres contextuelles](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) du panneau d’informations exige le serveur d’infos version 2.1.8 ou ultérieure.
* Search composants de fonctionnalités nécessitent S7Search 2.3.0 ou une version ultérieure.

## Configuration requise pour les visionneuses {#section-cc72b1e209524d038b4d5b92b35e998e}

**Configuration minimale requise pour le navigateur client pour les visionneuses de composants :**

* Pris en charge sur les versions de système d’exploitation suivantes ou ultérieures :
   * Microsoft® Windows® 7
   * macOS X 10.12
* Pris en charge sur les versions suivantes du navigateur/de la plate-forme ou versions ultérieures :
   * Android™ OS 4.x
   * BlackBerry® 10 sur les navigateurs natifs. Seule la lecture vidéo est prise en charge.
   * Chrome 82
   * Bord
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (navigateurs Safari et Chrome uniquement)
   * iPhone 3GS
   * Safari 11
* Internet Explorer sur les appareils mobiles n’est pas pris en charge.
* *PanoramicViewer* est pris en charge sur les versions suivantes du navigateur/de la plate-forme ou versions ultérieures :
   * Android™ 4.4 (appareils téléphoniques uniquement)
   * Chrome 82
   * Bord
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* et *DimensionalViewer* sont pris en charge sur les versions suivantes du navigateur/de la plate-forme ou versions ultérieures :
   * Android™ 5 (appareils téléphoniques uniquement)
   * Chrome 82
   * Bord
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* est pris en charge sur les versions suivantes du navigateur/de la plate-forme ou versions ultérieures :
   * Android™ 4.x
   * Chrome 82
   * Bord
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## Fin de la prise en charge de TLS 1.0 et 1.1 {#tls}

<!-- CQDOC-19433 -->

À compter du 30 septembre 2022, Adobe Dynamic Media Les visionneuses ont cessé de prendre en charge les éléments suivants :

* TLS (Transport Layer Security) 1.0 et 1.1
* Les chiffrements faibles suivants dans TLS 1.2 :
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Combinaisons de navigateur Web et de système d’exploitation non prises en charge par les visionneuses Dynamic Media {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media Les visionneuses ne prennent pas en charge les combinaisons suivantes de navigateur Web et de système d’exploitation :

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Mise à jour d’Internet Explorer 11 + Windows Phone 8.1
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android&trade; 2.3.7
* Android&trade; 4.0.4
* Android&trade; 4.1.1
* Android&trade; 4.2.2
* Android&trade; 4.3
* Internet Explorer 7 on Window Vista&reg;
* Internet Explorer 8 on Windows&reg; XP
* Internet Explorer 8-10 on Windows&reg; 7
* Internet Explorer 10 on Windows&reg; Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java&trade; 6u45
* Java&trade; 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

