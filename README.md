# TP

#### Découvrir les webservices avec PHP et jQuery  

#### Objectifs :  
+ Savoir créer un webservice
+ Savoir accéder à un webservice
+ Encoder des données
+ Décoder des données
+ Traiter des données d’un webservices
+ Connaître les différents formats de sorties d’un webservice
+ Passer outre la sécurité des navigateurs
+ Créer un proxy en PHP

## Exercice 1 : Ecrire dans un fichier  
### Test N°1 : écrire dans un fichier txt 

Créer un fichier.txt contenant 3 prénoms  

**Travail à réaliser :**
+ Réaliser un script PHP qui lire le fichier  
+ Ajouter au fichier.txt un nouveau prénom  


**Indice :**
+ file_get_contents  

### Test N°2 : écrire dans un fichier log avec la méthode fopen
Créer un fichier.txt contenant 3 prénoms  

**Travail à réaliser :**
+ Réaliser un script PHP qui créer le fichier à la volée  
+ Ouvrir le fichier.log  
+ Ecrire dans le fichier.log une nouvelle entrée  
+ Fermer le fichier  



**Indice :**  
+ Il n’est pas obligatoire de créer le fichier en amont  

## Exercice 2 : Créer son propre webservice  
### Préparation  
Via une requête de sélection, récupérer dans une base de données 5 articles d’un blog fictif. Afficher ensuite le résultat sous forme de JSON.  

Il devra y avoir au minimum les champs suivants :  

+ Un titre  
+ Un texte de minimum 10 caractères  
+ Une date au format lisible Américain  

**Indice :**
+ json encode  
+ Header application/json  
+ Pas d’HTML  

### Test N°1 : Récupérer son webservices
Récupérer à l’aide de jQuery le résultat du JSON créé précédemment.  

**Travail à réaliser :**
+ Lors du clic sur le bouton « récupérer articles » la réponse dans la console du navigateur  
+ Afficher ensuite proprement la liste des articles dans la page en cours

**Indice :**
+ Console.log  
+ Fonction Ajax de jQuery  
+ Type GET  

### Test N°3 : Insérer dans une base de données  
Créer un script PHP qui va, lors de son appel, insérer des données dans une base de données. Nous restons sur le thème des articles de blog.   

**Travail à réaliser :**
+ Lors du clic sur le bouton « insérer un nouvel article » l’insertion doit se déclencher  
+ Insérer un nouvel article dans la base de données  
+ Afficher le résultat ainsi que les données nouvellement insérées  

**Indice :**
+ Type POST  

## Exercice 3 : Les webservices déjà existants
### Préparation

*A définir*

### Test N°1 : Récupérer les données d’un webservices gérant le JSONP  
Flickr  

**Travail à réaliser :**
+ Récupérer l’url du webservice au format JSONP
+ Récupérer en Ajax le résultat de l’appel de l’URL  
+ Récupérer le nom du groupe pour chaque groupe de parking (voir doc API)  
+ Tester avec différentes fonctions  
    + jQuery$.ajax()  
    + $.get()  
    + $.getJson()  

### Test N°2 : Récupérer les données d’un webservice au format JSON (Cross Domain Security)  

[URL API Nantes](http://data.nantes.fr/donnees/choix-des-formats/)  
[URL pour l’exercice](http://data.nantes.fr/donnees/fonctionnement-de-lapi/getdisponibiliteparkingspublics/)  

**Travail à réaliser :**
+ Récupérer l’url du webservice au format JSON
+ Récupérer en Ajax le résultat de l’appel de l’URL 
+ Récupérer le nom du groupe pour chaque groupe de parking (voir doc API)
+ Tester avec différentes fonction jQuery

**Indice :**
+ Security Cross Domain à désactiver
+ Propriétés Raccourci Chrome & web Security  

### Test N°3 : Récupérer les données d’un webservice au format JSON (Proxy)  
[URL API Nantes](http://data.nantes.fr/donnees/choix-des-formats/)

**Travail à réaliser :**
+ Récupérer l’url de l’exercice précédent
+ Récupérer le résultat de l’appel de l’URL via Ajax et Proxy PHP
+ Récupérer le nom du groupe et le nombre de places disponibles pour chaque groupe de parking (voir doc API)

**Indice :**
+ Proxy en PHP
+ Appel du Proxy en Ajax
+ Deux URL en une seule, une URL qui en cache une autre
+ Attribut « data » de la fonction ajax en jQuery

### Test N°4 : Récupérer les données d’un webservice au format JSON (Proxy) et les insérer dans une base de données
[URL API Nantes](http://data.nantes.fr/donnees/choix-des-formats/)  

** Travail à réaliser : **  

+ Même travail que précédemment
+ Récupérer des données, les traiter et les stocker en base de données. (système de cache PHP, chercher PHP Proxy Cache, github)
