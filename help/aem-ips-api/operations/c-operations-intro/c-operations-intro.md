---
description: Cette section décrit les paramètres d'opération courants gérés par l'API Service Web IPS.
seo-description: Cette section décrit les paramètres d'opération courants gérés par l'API Service Web IPS.
seo-title: Méthodes d'exploitation
solution: Experience Manager
title: Méthodes d'exploitation
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# Méthodes d&#39;exploitation{#operations-methods}

Cette section décrit les paramètres d&#39;opération courants gérés par l&#39;API Service Web IPS.

Pour une description complète de chaque paramètre d’opération, voir Paramètres [d’](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)opération.

## Poignées : À propos de {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gère les objets IPS de référence renvoyés par certaines opérations d&#39;API. Vous pouvez également transmettre des poignées en tant que paramètres aux appels d’opération suivants. Les poignées sont des types de données de chaîne ( `xsd:string`).

Les poignées sont destinées à être utilisées au cours d’une seule session d’application. En outre, vous devez rendre les poignées persistantes car leur format peut changer d&#39;une version d&#39;IPS à l&#39;autre. Lorsque vous créez des applications interactives, vous mettez en oeuvre des délais d’expiration de session et ignorez toutes les poignées entre les sessions, en particulier après une mise à niveau d’IPS. Lorsque vous écrivez des applications non interactives, appelez les opérations appropriées pour récupérer les poignées chaque fois que l’application est exécutée. Les exemples de code Java/Axis2 suivants montrent une exécution de code incorrecte et correcte :

**Code de poignée incorrect**

Cet exemple de code est incorrect, car il contient une valeur codée en dur (555) pour la poignée de  du.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Code de poignée correct**

Cet exemple de code est correct car il appelle `getCompanyInfo` pour renvoyer un handle valide. Elle ne repose pas sur une valeur codée en dur. Utilisez cette méthode ou un autre équivalent d&#39;API IPS pour renvoyer la poignée requise.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Types de poignée courants {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

Pour la plupart des opérations, vous devez définir un contexte de  en transmettant un `companyHandle` paramètre. La poignée  est un pointeur renvoyé par certaines opérations, telles que `getCompanyInfo`, `addCompany`et `getCompanyMembership`.

**userHandle**

Le `userHandle` paramètre est facultatif pour les opérations qui  un utilisateur spécifique. Par défaut, ces opérations  l’utilisateur appelant (l’utilisateur dont les informations d’identification sont transmises pour authentification). Toutefois, les administrateurs disposant des autorisations appropriées peuvent spécifier un autre utilisateur. Par exemple, l’ `setPassword` opération définit normalement le mot de passe de l’utilisateur authentifié, mais un administrateur peut utiliser le `userHandle` paramètre pour définir le mot de passe d’un autre utilisateur.

Pour les opérations qui nécessitent un contexte de  (à l’aide du `companyHandle` paramètre), les utilisateurs  authentifiés et doivent tous deux être membres de l’ spécifiée. Pour les opérations qui ne nécessitent pas de contexte de , les utilisateurs authentifiés et les utilisateurs  doivent tous deux être membres d’au moins une  commune.

Les opérations suivantes peuvent récupérer les poignées utilisateur :

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle et accessGroupHandle**

Par défaut, les opérations qui nécessitent des autorisations d’accès (lecture, écriture, suppression) fonctionnent dans le contexte des autorisations de l’utilisateur appelant. Certaines opérations vous permettent de modifier ce contexte avec le `accessUserHandle` paramètre ou `accessGroupHandle` . Le `accessUserHandle` paramètre permet à un administrateur d’emprunter l’identité d’un autre utilisateur. Le `accessGroupHandle` paramètre permet à l’appelant de fonctionner dans le contexte d’un groupe d’utilisateurs spécifique.

**responseFieldArray et excludeFieldArray**

Certaines opérations permettent à l’appelant de limiter les champs inclus dans la réponse. Le fait de limiter les champs permet de réduire le temps et la mémoire nécessaires au traitement de la requête et de réduire la taille des données de réponse. L’appelant peut demander un spécifique de champs en transmettant un `responseFieldArray` paramètre ou avec un énuméré de champs exclus via le `excludeFieldArray` paramètre.

Les deux `responseFieldArray` champs et `excludeFieldArray` spécifiez-les en utilisant un chemin de noeud séparé par `/`. Par exemple, pour indiquer que `searchAssets` renvoie uniquement le nom, la date de dernière modification et les métadonnées de chaque fichier, reportez-vous aux éléments suivants :

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

De même, pour renvoyer tous les champs (à l’exception des autorisations) :

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Notez que les chemins d’accès au noeud sont relatifs à la racine du noeud de retour. Si vous spécifiez un champ de type complexe sans aucun de ses sous-éléments (par exemple `assetArray/items/imageInfo`), tous ses sous-éléments sont inclus. Si vous spécifiez un ou plusieurs sous-éléments dans un champ de type complexe (par exemple `assetArray/items/imageInfo/originalPath`), seuls ces sous-éléments sont inclus.

Si vous n’incluez pas `responseFieldArray` ou `excludeFieldArray` dans une requête, tous les champs sont renvoyés.

**Paramètres régionaux**

Depuis IPS 4.0, l’API IPS prend en charge la définition du contexte régional d’une opération en transmettant le paramètre `authHeader` régional. Si le paramètre régional n’est pas présent, l’en-tête HTTP `Accept-Language` sera utilisé. Si cet en-tête n&#39;est pas non plus présent, les paramètres régionaux par défaut du serveur IPS sont utilisés.

Certaines opérations utilisent également des paramètres régionaux explicites, qui peuvent être différents du contexte régional de l’opération. Par exemple, l’ `submitJob` opération utilise un `locale` paramètre qui définit les paramètres régionaux utilisés pour la journalisation des tâches et la notification par courrier électronique.

Les paramètres régionaux utilisent le format `<language_code>[-<country_code>]`

Lorsque le code de langue est un code à deux lettres en minuscules spécifié par ISO-639 et que le code de pays facultatif est un code à deux lettres en majuscules spécifié par ISO-3266. Par exemple, la chaîne de paramètres régionaux pour l’anglais américain est `en-US`.
