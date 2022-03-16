# Apache HTTP Server

Le TP est à effectuer sur Linux CentOS 7.

## 1. Installation

- Installer et lancer le serveur _Apache HTTP Server_
- _Sur la machine CentOS_, tester le service en affichant la page de test d'_Apache HTTP Server_ (ouvrir l'URL `localhost`)
- Effectuer les modifications pour pouvoir accéder à cette page _depuis le navigateur du système hôte_

## 2. Configuration du site Web

On souhaite que notre page d'accueil s'affiche, plutôt que la page de test.

- Localiser le fichier de configuration d'Apache et y trouver les informations suivantes :
  - le port par défaut sur lequel le serveur va « écouter » les requêtes HTTP
  - le nom des pages par défaut que Apache recherchera et affichera
  - le répertoire dans lequel les fichiers du site sont localisés par défaut
- Créer un fichier HTML basique correctement formaté et contenant un `title` et un `body` avec une balise `h1` et un paragraphe
- Faire en sorte que ce soit la page dorénavant affichée lorsque l'on visite la racine du serveur

## 3. Virtual Hosts

On souhaite que le server soit capable d'héberger plusieurs sites afin de réduire les coûts.

- Faire en sorte que soient servis les deux domaines suivants (avec des pages par défaut indiquant clairement de quel domaine il s'agit) en configurant des *Virtual Hosts* :
  - `www.mondomaine.net`
  - `www.mondomaine.fr`
- Faire en sorte que, en local, l'accès à ces deux domaines soient redirigés sur l'ip du serveur Web
- Redémarrer le serveur et tester
  - l'accès à `www.mondomaine.net` arrive sur une page « Bienvenue sur mondomaine.net ! »
  - l'accès à `www.mondomaine.fr` arrive sur une page « Bienvenue sur mondomaine.fr ! »
- Vérifier les accès (requêtes HTTP GET) dans les fichiers de log

## 4. Transfert des droits

- Transférer les droits sur les deux sites depuis _root_ vers un utilisateur basique

## 5. Support PHP

- Mettre en place le support de PHP sur le serveur
- Effectuer les modifications nécessaires pour pouvoir tester la bonne mise en place de PHP

## 6. Contrôle d'accès basé sur l'hôte

On veut restreindre l'accès au serveur sur la base de l'adresse IP.

- Faire en sorte que votre machine hôte (Windows ou Linux) ne puisse pas accéder à l'adresse `www.mondomaine.net` mais conserve l'accès à l'autre site
- Vérifier les accès dans les fichiers de log : comment sait-on que l'un des accès a été refusé ?
- Maintenant, on souhaite que _seule la machine hôte_ ait accès à l'adresse `www.mondomaine.fr` (toutes les autres requêtes doivent être refusées) ; modifier la configuration en conséquence

## Contrôle d'accès basé sur l'utilisateur

On veut restreindre l'accès à seulement certains utilisateurs par une authentification basique (_Authtype Basic_). Le navigateur devra afficher une popup d'accès restreint en demandant un nom d'utilisateur et un mot de passe.

- Mettre en place ce contrôle d'accès pour `www.mondomaine.fr` avec un utilisateur appelé `admin`
