---
description: Contient les paramètres de configuration du superviseur du serveur.
seo-description: Contient les paramètres de configuration du superviseur du serveur.
seo-title: SupervisorRegistry.xml
solution: Experience Manager
title: SupervisorRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 8442a3d6-5f45-48d1-8e6e-71f0ed384227
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# SupervisorRegistry.xml{#supervisorregistry-xml}

Contient les paramètres de configuration du superviseur du serveur.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, sans quoi le serveur d’images risque de ne pas se début.

Redémarrez la diffusion d’images après avoir modifié ce fichier pour vous assurer que vos modifications prennent effet. Seules les valeurs d’élément/d’attribut surlignées ci-dessous sont prises en charge pour modification. Modifiez tous les autres contenus de ce fichier uniquement si le support technique de Scene7 vous en informe.

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Scene7 Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Scene7 SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Scene7 Platform Server</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```

