# Reading user input ⌨️

Pour lire une entrée utilisateur depuis la ligne de commande, nous allons utiliser le module standard `io`

```rust 
use std::io;
```

Maintenant, nous avons besoin d'une variable pour stocker l'entrée utilisateur.

```rust
let mut input = String::new();
```

Et nous avons besoin d'afficher un message pour demander a l'ulisateur d'entrer une valeur.

```rust
println!("Entrez votre nom: ");
```

Finalement, nous allons lire l'entrée utilisateur avec la method `stdin().read_line()`

```rust
io::stdin().read_line(&mut input);
// on donne une reference mutable de la variable input a la fonction
```

La fonction `read_line` retourne une valeur de type `Result`, c'est un type qui peut représenter une valeur, ou une erreur.

Nous allons donc faire un match sur ce type de retour.

```rust
match io::stdin().read_line(&mut input) {
    Ok(_) => {
        println!("Bonjour, {}", input);
    },
    Err(error) => {
        println!("Erreur: {}", error);
    }
}
```

On met un `_` en parametre de la cranche `Ok` pour ignorer la valeur retournée par la fonction `read_line`, il s'agit du nombre de caracteres lus.

Nous pouvons maintenant executer le programme.

```bash
$ cargo run
Entrez votre nom:
> John 
Bonjour, John
```

<!--
---

<p align="right"><a href="https://skwalexe.github.io/apprendre-rust/">Accueil 🏠</a> - <a href="../les-vecteurs">Section suivante ⏭️</a></p>
-->

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>