# Sommaire📚
- [Qu'est ce que c'est ❓](#quest-ce-que-cest)
- [Comment ça marche 🤔](#comment-ca-marche)

# Shadowing👥
## Qu'est ce que c'est❓
Quand on modifie une variable existante dans un code block, la modification reste à l'extérieur du code block, mais il est possible de faire revenir la variable à sa valeur d'origine quand le code block se termine. C'est appelé shadowing.

## Comment ca marche🤔
Par exemple, on peut utiliser un code block pour modifier une variable:
```rust
let worm_name = "Wormie 🪱";

{
    worm_name = "Wormy 🪱";
    println!("Mon verre de terre s'appelle {}", worm_name);
}

println!("Mon verre de terre s'appelle {}", worm_name);
```
Output:
```
Mon verre de terre s'appelle Wormy 🪱
Mon verre de terre s'appelle Wormy 🪱
```

Nous pouvons voir que la modification de la variable `worm_name` est toujours disponible à l'extérieur du code block. Nous pouvons shadow la variable avec une nouvelle variable dans le code block en ajoutant le mot-clé `let` avant le nom de la variable.

```rust
let worm_name = "Wormie 🪱";

{
    let worm_name = "Wormy 🪱";
    println!("Mon verre de terre s'appelle {}", worm_name);
}

println!("Mon verre de terre s'appelle {}", worm_name);
```
Output:
```
Mon verre de terre s'appelle Wormie 🪱
Mon verre de terre s'appelle Wormy 🪱
```

<!--

---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/shadowing">Section suivante ⏭️</a></p>
-->

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>