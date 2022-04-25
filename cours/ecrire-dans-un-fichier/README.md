# Sommaire📚

- [Creer un fichier](#creer-un-fichier)
- [Ecrire dans un fichier ✏️](#ecrire-dans-un-fichier-️)

# Ecrire dans un fichier ✍️

## Creer un fichier 

Tout d'abord, nous allons importer les modules nécessaires pour effectuer des opérations sur les fichiers.

```rust
use std::fs::File;
use std::io::prelude::*;
```

Pour créer un fichier, on utilise la methode `create` de `File`.

```rust
let mut file = File::create("hello.txt").expect("impossible de créer le fichier");
```

On spécifie le nom du fichier en tant que paramètre de la methode `create`.

Maintenant essayons d'executer le programme.

```
$ cargo run
```

Nous pouvons maintenant voir a la racine du projet, le fichier `hello.txt`, vide.

## Ecrire dans un fichier ✏️

Ecrivons maintenant `Hello World` dans le fichier.

pour ca, on utilise la methode `write_all`.

```rust
file.write_all(b"Hello World").expect("impossible d'ecrire dans le fichier");
```

Le programme ignore si le fichier existe deja quand il essaye de le creer.

dans la fonction `write_all`, on ajoute un `b` devant le texe à écrire pour le transformer en un array d'octets car la fonction `write_all` prend en paramètre un `&[u8]`.

La methode `write_all` va écraser le contenu du fichier a chaque écriture.

Maintenant si nous executons a nouveau le programme, nous pouvons voir le contenu du fichier :

```
$ cargo run
```

```
Hello World
```

<!--
---

<p align="right"><a href="https://skwalexe.github.io/apprendre-rust/">Accueil 🏠</a> - <a href="../les-vecteurs">Section suivante ⏭️</a></p>
-->

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>