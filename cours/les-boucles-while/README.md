# Sommaire📚
- [Qu'est ce qu'une boucle while](#quest-ce-quune-boucle-while)
- [Le mot clé `while`](#le-mot-cle-while)
- [Les mots clés `break` et `continue`](#les-mots-cles-break-et-continue)
# Les boucles while🔁
## Qu'est ce qu'une boucle while?
Les boucles while permettent d'executer un block de code aussi longtemps qu'une condition est vraie.
## Le mot cle while
Le mot clé while eest utilisé pour créer une boucle while.

exemple:

```rust
let mut count = 0;

while count < 5 {
    println!("{}", count);

    // Incrementer `count`
    count += 1;
}
```
Tant que la valeur de `count` est inférieure à 5, nous afficherons sa valeur, puis nous incrémenterons `count` de 1.

Sortie:
```
0
1
2
3
4
```
## Les mots cles break et continue
Nous pouvons aussi utiliser les mots clé `break` et `continue` comme vu dans la section [Les boucles infinies♾️](https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-boucles-infinies).

<!--

---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/hello-world">Section suivante ⏭️</a></p>
-->

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>