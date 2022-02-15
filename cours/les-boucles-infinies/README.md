# Sommaire📚
- [Qu'est-ce qu'une boucle infinie ?](#quest-ce-quune-boucle-infinie)
- [Le mot clé `loop`](#le-mot-cle-loop)
- [Le mot clé `break`](#le-mot-cle-break)
- [Le mot clé `continue`](#le-mot-cle-continue)

# Les boucles infinies♾️
## Qu'est ce qu'une boucle infinie?
Les boucles infinies nous permettent d'executer un bloque de code a l'infini jusqu'a ce que l'on spécifie quand l'arreter
## le mot cle loop
Pour créer une boucle infinie, on utilise le mot clé loop 

exemple, afficher `Rust rocks` a l'infini:
```rust
loop {
    println!("Rust rocks");
}
```
Sortie:
```
Rust rocks
Rust rocks
Rust rocks
Rust rocks
...
```
## Le mot cle break
le mot clé `break` permet d'arreter l'execution d'une boucle.
Imaginons vouloir afficher `Rust rocks` 5 fois, puis stoper l'execution de la boucle.
```rust
let mut i = 0;
loop {
    println!("Rust rocks");
    i += 1;
    if i == 5 {
        break;
    }
}
```
On ajoute 1 a la cariable `count` a chaque tour de boucle, et, quand `count` est égale a 5, on arrete la boucle.
Sortie:
```
Rust rocks
Rust rocks
Rust rocks
Rust rocks
Rust rocks
```

## Le mot cle continue
le mot clé `continue` permet de passer directement a la prochaine iteration de la boucle.
> ℹ️ une iteration correspond a une execution individuelle de la boucle.
Imaginons que nous voulons dire "Hello" 5 fois, mais que nous voulons ignorer le deuxieme
```rust
let mut i = 0;
loop {
    i += 1;
    if i == 2 {
        continue;
    }
    println!("{} : Hello", i);
    if i == 5 {
        break;
    }
}
```

> ℹ️ `count += 1` est equivalent a `count = count + 1`

On ajoute 1 a la cariable `count` a chaque tour de boucle, et, quand `count` est égale a 2, on passe directement a la prochaine iteration de la boucle sans dire "Hello".

Sortie:
```
1 : Hello
3 : Hello
4 : Hello
5 : Hello
```


<!--

---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/hello-world">Section suivante ⏭️</a></p>
-->

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>