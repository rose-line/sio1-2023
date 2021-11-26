# Deviner le nombre

## Présentation

Le but est de programmer un tout petit jeu sur le terminal, une sorte  de « Devinez le nombre ». Une fois terminé, ça ressemble à ça :

```
Je pense à un nombre entre 1 et 100 inclus. Devinez lequel.
Entrez un nombre : 36
Vous proposez : 36
Le nombre auquel je pensais était : 47
Vous étiez à 11 de la bonne réponse.
```

Vous aurez besoin d'un objet de la classe `Scanner` pour prendre une entrée au clavier. Sur un tel objet (ci-dessous nommé `scan`), on peut appeler des méthodes du style `nextInt()` pour récupérer un entier, `nextDouble()` pour récupérer un nombre flottant, `nextLine()` pour récupérer une chaîne de caractère, etc.

```java
Scanner scan = new Scanner(System.in);  // System.in : indique que l'on "scanne" le clavier
int texte = scan.nextLine();
System.out.println("Vous avez écrit : " + texte);
```

NB : Pour que ça fonctionne effectivement avec VS Code, il y aura peut-être une petite modification à effectuer : ouvrez `launch.json` (le fichier des configurations de lancement, trouvé dans le répertoire `.vscode` ou en cliquant sur le bouton "rouage" dans le panneau de débogage), et changez le paramètre `"console": "internalConsole"` en `"console": "integratedTerminal"`. Cela va forcer la sortie de votre programme sur le terminal intégré plutôt que sur la console de débogage intégrée (qui ne gère pas les entrées au clavier).

Vous aurez également besoin de générer un nombre aléatoire entre 1 et 100, comme ceci :

```java
Random random = new Random();
int nombre = random.nextInt(100) + 1;  // nextInt(n) renvoie un entier entre 0 et n-1
System.out.println(nombre);
```

## Implémentation

Implémentez le programme pour obtenir le comportement décrit dans l'exemple du début. Testez chaque partie du code au fur et à mesure.

## Évolutions

- Faites en sorte que la partie « entrée » soit faite dans une méthode à part.

- Faites en sorte que le programme demande si le joueur veut rejouer à la fin d'une partie. La boucle `while` sera plus pratique que la boucle `for` pour ce genre de traitement :

```java
onContinue = true;
while(onContinue) {   // TANT QUE onContinue est vrai, on exécute le corps de la boucle
  // Traitement à répéter
  // Il n'a a pas de mise à jour de la variable dans la syntaxe de la boucle while (contrairement à for)
  // Il faut mettre à jour la variable de test "à la main" dans le corps pour que la boucle finisse par s'arrêter
  
  if ("les conditions sont réunies pour s'arrêter") {
    onContinue = false;
  }
}
```
