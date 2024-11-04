#Créer un plugin WordPress pour limiter la taille des titres à 80 caractères afin de pouvoir automatiser un blog sans tout casser. Voici un guide étape par étape pour créer ce plugin.
Je partage ici tous le soutils bricolés pour mes campagnes seo pour [internet communication](https://www.internetcommunication.fr)

> *Pré-requis* : à tester dans un environnement de préprod.

###Étape 1: Créez un dossier pour le plugin : Créez un nouveau dossier dans le répertoire /wp-content/plugins/ de votre installation WordPress. Nommez-le par exemple "limiter-taille-titres".
###Étape 2: Créez le fichier principal du plugin : Dans le dossier "limiter-taille-titres", créez un fichier PHP nommé "limiter-taille-titres.php".
###Étape 3: Ajoutez les en-têtes du plugin : Ouvrez le fichier "limiter-taille-titres.php" et ajoutez les en-têtes de plugin suivants:

php


/*
Plugin Name: Limiter Taille Titres
Plugin URI: https://exemple.com/limiter-taille-titres
Description: Limite la taille des titres à 80 caractères
Version: 1.0
Author: Votre nom
Author URI: https://exemple.com
License: GPLv2 or later
Text Domain: limiter-taille-titres
*/

###Étape 4: Ajoutez le code pour limiter la taille des titres : Ajoutez le code suivant dans le fichier "limiter-taille-titres.php" pour limiter la taille des titres à 100 caractères:

php

function ltt_limiter_taille_titres($title) {
    return substr($title, 0, 100);
}
add_filter('the_title', 'ltt_limiter_taille_titres');

/*Cette fonction utilise le filtre 'the_title' pour appliquer la limitation de taille sur tous les titres affichés sur le site.

###Étape 5: Activez le plugin : Connectez-vous à votre tableau de bord WordPress, allez dans "Extensions", recherchez "Limiter Taille Titres" dans la liste des plugins, et activez-le.

###Maintenant, tous les titres affichés sur votre site seront automatiquement limités à 80 caractères. Notez que cela n'affecte pas les titres enregistrés dans la base de données, mais seulement leur affichage sur le site.

###Je vais proposer mes autres plugins si cela peut aider
