---
title: en-tête
description: Élément d’en-tête de réponse HTTP. Facultatif dans les éléments <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
TQID: 'https://experienceleague.adobe.com/-hGRn7zVjm8eavZIwBoiAuCqoSNYIFSSlQaSP6wuHXs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 2%

---

# en-tête{#header}

Élément d’en-tête de réponse HTTP. Facultatif dans les éléments `<rule>`.

## Attributs {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= « *text*«** : obligatoire. Indique le nom de l’en-tête HTTP.

**`Action`= « set » |`"add"`** : facultatif. La valeur par défaut est `"set"`, ce qui remplace toute valeur d’en-tête actuelle. Spécifiez `"add"` afin de pouvoir ajouter la valeur de l’en-tête, séparée par une virgule.

## Données {#section-a387f541396c49d99c29692a38032914}

Valeur de l’en-tête.

## Description {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permet d’ajouter de nouveaux en-têtes de réponse HTTP et d’ajouter ou de remplacer des valeurs d’en-têtes prédéfinis. Les noms et les valeurs doivent être conformes aux normes HTTP. Aucun encodage supplémentaire n’est appliqué.

Les variables de substitution de diffusion d’images peuvent être utilisées dans le nom et la valeur de l’en-tête. Cela permet de contrôler les deux chaînes à partir de la requête.

## Exemple {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La règle suivante applique un en-tête personnalisé lorsque la valeur de l’en-tête est spécifiée dans la requête en tant que variable :

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Cette règle est déclenchée par la requête suivante, définissant la `Edge-Control::no-store` d’en-tête de réponse HTTP :

`http://server/is/image/cat/id?$Edge-Control=no-store`
