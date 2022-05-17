# Sommaire📚

- [Le mot clé match 🔍](#le-mot-clé-match-)
- [Multiple patterns](#multiple-patterns)
- [Verifier si une valeur est dans une intervalle](#verifier-si-une-valeur-est-dans-une-intervalle)

# Le mot clé match 🔍

## Le mot clé match 🔍


Le mot clé `match` est similaire aux `switch` en d'autres langages.

C'est un operateur conditionnel qui permet de faire differentes choses en fonction d'une valeur.

par exemple : 

```rust
let nombre = 2;

match nombre {
    1 => println!("le nombre est 1"),
    2 => println!("le nombre est deux"),
    3 => {
        println!("le nombre est 3");
        println!("le nombre est encore 3");
      },
    _ => println!("le nombre n'est pas un, deux ou trois")
}
```

Les valeurs que l'on compare (1, 2, 3) sont les patterns.

Le `_` est un jocker, il sera utilisé si aucune correspondance n'est trouvée.

Vous devez ajouter des `{}` si vous voulez executer plusieurs lignes de code.

La valeur et les patters doivent etre du meme type de donnée.

Si nous executons le programme : 

```bash
$ cargo run
> le nombre est deux
```

## Multiple patterns

On peut comparer plusieurs patterns avec le `|`

```rust
let nombre = 3;

match nomlbre { 
    1 | 3 => println!("le nombre est 1 ou 3"),
    _ => println!("Le nombre n'est pas un ou trois")
}
```

```bash
$ cargo run
> le nombre est 1 ou 3
```

## Verifier si une valeur est dans une intervalle 

Nous pouvons egalement verifier si une valeur est dans une intervalle.

```rust
let nombre = 4;

match nombre { 
    1...5 => println!("le nombre est entre un et cinq"),
    _ => println!("le nombre n'est pas entre un et cinq")
}
```

Si nous executons le programme : 

```bash
$ cargo run
> le nombre est entre un et cinq
```


<!--
---

<p align="right"><a href="https://skwalexe.github.io/apprendre-rust/">Accueil 🏠</a> - <a href="../les-vecteurs">Section suivante ⏭️</a></p>
-->

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>