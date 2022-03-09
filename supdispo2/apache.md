# Apache HTTP Server

Le TP est à effectuer sur Linux CentOS 7.

## 1. Installation

- Installer et lancer le serveur _Apache HTTP Server_
- Tester le service en affichant la page de test d'_Apache HTTP Server_ (ouvrir l'URL `localhost`)

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

## 4. Support PHP

- Mettre en place le support de PHP sur le serveur
- Effectuer les modifications nécessaires pour pouvoir tester la bonne mise en place de PHP
