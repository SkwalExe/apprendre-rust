# Sommaire📚
- [Qu'est ce qu'une boucle while ❓](#quest-ce-quune-boucle-while)
- [Le mot clé `while` 🔁](#le-mot-cle-while)
- [Les mots clés `break` et `continue` 🔑](#les-mots-cles-break-et-continue)
# Les boucles while🔁
## Qu'est ce qu'une boucle while❓
Les boucles while permettent d'executer un block de code aussi longtemps qu'une condition est vraie.
## Le mot cle while🔁
Le mot clé while est utilisé pour créer une boucle while.

Exemple:

```rust
let mut count = 0;

while count < 5 {
    println!("J'ai {} 😺 Chats", count);

    // Incrementer `count`
    count += 1;
}
```
Tant que la valeur de `count` est inférieure à 5, nous afficherons `J'ai x 😺 Chats`, puis nous incrémenterons `count` de 1.

Sortie:
```
J'ai 0 😺 Chats
J'ai 1 😺 Chats
J'ai 2 😺 Chats
J'ai 3 😺 Chats
J'ai 4 😺 Chats
```
## Les mots cles break et continue🔑
Nous pouvons aussi utiliser les mots clé `break` et `continue` comme vu dans la section [Les boucles infinies♾️](https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-boucles-infinies).


---

<p align="right"><a href="../les-boucles-for">Section suivante ⏭️</a></p>


---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>