# TP jQuery

Les fonctionnalités ci-dessous peuvent être réalisées en JS pur, voire en CSS pur. Pour ce TP, il vous est demandé de les réaliser avec jQuery (l'utilisation d'attributs `id` ou de `class` est bien entendu autorisé dans le HTML).

## 1. Menu _dropdown_

- Créez une page web ou reprenez une page web existante sur l'un de vos projets.
- Créez un menu _dropdown_ contenant des liens vers d'autres pages du site.
  - je clique sur le menu _dropdown_, trois possibilités s'affichent
  - si je reclique ailleurs sur la page, le menu disparaît
  - mais si je clique sur l'une des trois possibilités, le lien correspondant est suivi
- Mots-clés jQuery : `mouseover(), show(), mouseout()`

## 2. Convertisseur

- Ajoutez à une page de votre site un module de conversion (choix entre deux possibilités, voir plus bas)
- Deux _fields_ sont affichés (gauche/droite)
  - à gauche, vous entrez la valeur à convertir
  - lorsque le focus change, la valeur convertie (à droite) s'affiche
- Une fois cette partie terminée, faites en sorte que la conversion s'applique _dans les deux sens_ (si vous modifiez à droite, ça se met à jour à gauche)
- Puis modifiez le code pour que les conversions se fassent en temps réel, en même temps que la frappe
- Choisissez votre niveau de difficulté :
  - niveau facile : conversion mètres <=> centimètres (2 donne 200 à droite et inversement)
  - niveau difficile : conversion couleur héxadécimale en couleur (#FF0000 affiche du rouge dans l'autre case, qui contient un _Color Picker_ HTML permettant de choisir une couleur dans une palette)
- Mots-clés jQuery : `change(), val(), input`

## 3. Validation de formulaire

Vous travaillez sur la page HTML fournie ci-dessous. L'utilisateur doit fournir les informations suivantes, avec les contraintes indiquées :

- *Identifiant client* : caractères alphanumériques (lettres et chiffres) ; ne peut être vide
- *Mot de passe* : au moins 12 caractères
- *Adresse email* : doit être une adresse valide ; ne peut être vide
- *Sélection de produits* : au moins un produit doit être sélectionné
- *Paiement* : un mode de paiement doit être sélectionné
- *Pays d'expédition* : un pays doit être sélectionné

Vous vous chargez de la partie validation client de ce formulaire, à l'aide de jQuery :

1. En cliquant sur « Commander », l'utilisateur est notifié des erreurs de validation potentielles par des messages d'erreurs apparaissant en rouge près des éléments HTML concernés.

2. Amélioration : l'utilisateur est notifié des erreurs pour les trois entrées du cadre « Vos informations » dès que le focus quitte l'élément `input` correspondant.

Page `validation.html` de base :

```html
<!DOCTYPE html>

<html lang="fr">
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>Validation jQuery</title>
    <link rel="stylesheet" href="style.css" type="text/css" media="screen" />
  </head>
  <body>
    <h1>Livraison rapide internationale</h1>
    <form>
      <fieldset>
        <legend>Vos informations</legend>
        <div>
          <span class="label">Identifiant client</span>
          <input type="text" name="idclient" />
        </div>
        <div>
          <span class="label">Mot de passe</span>
          <input type="password" name="mdp" />
        </div>
        <div>
          <span class="label">Adresse email</span>
          <input type="text" name="email" />
        </div>
      </fieldset>
      <br />
      <fieldset>
        <legend>Votre commande</legend>
        <div>
          <span class="label">Sélectionnez les produits :</span>
          <br />
          <br />
          <input
            type="checkbox"
            id="pizza"
            name="pizza"
            value="10"
            class="cb"
          />Pizza 10€<br />
          <input
            type="checkbox"
            id="hotdog"
            name="hotdog"
            value="4"
            class="cb"
          />Hot Dog 4€<br />
          <input
            type="checkbox"
            id="fites"
            name="frites"
            value="3"
            class="cb"
          />Frites 3€<br />
          <input
            type="checkbox"
            id="boisson"
            name="boisson"
            value="2"
            class="cb"
          />Boisson 2€<br />
        </div>
        <div>
          <span class="label">Paiement</span>
          <br />
          <input
            type="radio"
            name="paiement"
            class="radiobtn"
            value="Master Card"
          />Master Card<br />
          <input
            type="radio"
            name="paiement"
            class="radiobtn"
            value="Visa"
          />Visa<br />
          <input
            type="radio"
            name="paiement"
            class="radiobtn"
            value="Virement"
          />Virement<br />
        </div>
      </fieldset>
      <br />
      <fieldset>
        <legend>Expédition</legend>
        <div>
          <span class="label">Pays</span>
          <select class="selectbox">
            <option value="0">Pays d'expédition</option>
            <option value="France">France</option>
            <option value="Belgique">Belgique</option>
            <option value="Luxembourg">Luxembourg</option>
            <option value="Japon">Guyane</option>
          </select>
        </div>
      </fieldset>
      <input class="submit" type="submit" value="Commander" />
    </form>
  </body>
</html>
```

Fichier `style.css` associé :

```css
.submit {
  margin-left: 125px;
  margin-top: 10px;
}

.label {
  float: left;
  width: 120px;
}

.selectbox {
  width: 200px;
}

div {
  padding: 5px;
}

.cb {
  margin-left: 125px;
  margin-top: 10px;
}

.radiobtn {
  margin-left: 125px;
  margin-top: 10px;
}

.inputs {
  background-color: cyan;
}

fieldset {
  border: 1px solid #888;
}

legend {
  border: 1px solid #888;
  background-color: grey;
  color: white;
  font-weight: bold;
  padding: 0.5em;
}
```
