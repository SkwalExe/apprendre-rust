# Sommaire📚

- [Le mot clé `use`](#le-mot-clé-use)
- [Les methodes `open` et `expect`](#les-methodes-open-et-expect)
- [La methode `read_to_string`](#la-methode-read_to_string)


# Lire un fichier 📖

## Le mot clé `use`

Premièrement, nous avons besoin d'un fichier a lire, nous allons donc créer un nouveau fichier dans le dossier de notre projet.

```bash
# 📄 hello.txt
World, Hello 👋
```

Maintenant, nous allons lire le fichier et afficher son contenu.

Premièrement, nous allons importer le struct `File` depuis le module `std::fs`, qui est la bibliotheque standard pour gerer les fichiers.

Pour importer un élément, on utilise le mot clé `use`.

```rust
use std::fs::File;
```

Puis nous allons importer `std::io::prelude::*` pour nous permettre d'effectuer des opérations d'écritures et de lectures sur les fichiers.

```rust
use std::io::prelude::*;
```

Le `*` signifie que nous allons importer toutes les fonctions du module `std::io::prelude`.

## Les methodes `open` et `expect`

La methode `open` retourne une valeur de type `Result`, c'est un type qui représente soit une valeur, soit une erreur.

Nous pouvons utiliser la methode `expect` sur une valeur de type `Result` pour recuperer la valeur. Il s'agit d'une valeur de type `File`.

La methode `open` prend un chemin vers le fichier en argument.

```rust
let mut file = File::open("hello.txt").expect("Impossible d'ouvrir le fichier");
```

La methode `expect` est utilisee pour gerer les erreurs. 

Si le fichier ne peut pas etre ouvert, le programme `panic`. Par exemple si le fichier n'existe pas, le programme affiche ce message d'erreur et se terminera.

```
thread 'main' panicked at 'Impossible d'ouvrir le fichier: Os { code: 2, kind: NotFound, message: "No such file or directory" }', rust.rs:5:41
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
```

## La methode `read_to_string`

La methode `read_to_string` prend comme argument une référence mutable vers un `String` et retourne une valeur de type `Result`.

Cette fonction va lire le contenu du fichier et le stocker dans la variable passée en argument.

```rust
let mut content = String::new();
file.read_to_string(&mut content).expect("Impossible de lire le fichier");

println!("📄 contenu : {}", content);
```

Sortie :

```
📄 contenu : World, Hello 👋
```

---

<p align="right"><a href="https://skwalexe.github.io/apprendre-rust/">Accueil 🏠</a> - <a href="../arguments-de-ligne-de-commande">Section suivante ⏭️</a></p>

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>