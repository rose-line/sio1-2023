# TP jQuery

Les fonctionnalités ci-dessous peuvent être réalisées en JS pur, voire en CSS pur. Pour ce TP, il vous est demandé de les réaliser avec jQuery (l'utilisation d'attributs `id` ou de `class` est bien entendu autorisé dans le HTML).

## 1. Menu _dropdown_

- Créez une page web ou reprenez une page web existante sur l'un de vos projets.
- Créez un menu _dropdown_ contenant des liens vers d'autres pages du site.
  - je place la souris dessus, trois possibilités s'affichent
  - si je bouge la souris hors du _dropdown_, le menu disparaît
  - mais si je clique sur l'une des trois possibilités, le lien correspondant est suivi
- mots-clés jQuery : `mouseover(), show(), mouseout()`

## 2. Convertisseur

- Ajoutez à une page de votre site un module de conversion
- deux _fields_ sont affichés (gauche/droite)
  - à gauche, vous entrez la valeur à convertir
  - en tapant, la valeur convertie (à droite) s'affiche _en temps réel_
- Une fois cette partie terminée, faites en sorte que la conversion s'applique _dans les deux sens_ (si vous modifiez à droite, ça se met à jour à gauche)
- Choisissez votre niveau de difficulté :
  - niveau facile : conversion mètres <=> centimètres (2 donne 200 à droite et inversement)
  - niveau difficile : conversion couleur héxadécimale en couleur (#FF0000 affiche du rouge dans l'autre case - dans l'autre sens, vous pouvez utiliser un _Color Picker_ HTML pour choisir une couleur dans une palette)
- mots-clés jQuery : `change(), val()`
