# Sommaire📚
- [Qu'est ce qu'une fonction ❓](#quest-ce-quune-fonction)
- [Déclarer une fonction](#declarer-une-fonction)
- [Retourner des valeurs](#retourner-des-valeurs)


# Les fonctions🛠️
## Qu'est-ce qu'une fonction❓
Une fonction est un morceau de code qui prend une ou plusieurs valeurs en entrée et renvoie une ou plusieurs valeurs en sortie.
## Declarer une fonction
On déclare les fonctions avec le mot clé `fn`.
> Les fonctions doivent etre déclarées en dehors de la fonction main et avant d'etre appelées.
```rust
fn nom_de_la_fonction(parametre1: Type, parametre2: Type) {
    // corps de la fonction
}
```

Exemple, écrire une fonction appelée `hello` qui dit `🔔 C'EST L'HEURE DE MANGEEEER` x fois:
```rust
fn hello(x: i32) {
    for _ in 0..x {
        println!("🔔 C'EST L'HEURE DE MANGEEEER");
    }
}

fn main() {
    hello(5);
}
```
Sortie:
```
🔔 C'EST L'HEURE DE MANGEEEER
🔔 C'EST L'HEURE DE MANGEEEER
🔔 C'EST L'HEURE DE MANGEEEER
🔔 C'EST L'HEURE DE MANGEEEER
🔔 C'EST L'HEURE DE MANGEEEER
```

## Retourner des valeurs
Les fonctions peuvent renvoyer des valeurs avec le mot clé `return`.

Par exemple, créer une fonction `isEven` (`estPair` en englais) qui renvoie `true` ou `false` selon si la valeur est pair ou impair:
```rust
fn is_even(x: i32) -> bool {
    return x % 2 == 0
}
```
> ℹ️ On **doit** spécifier le type de retour de la fonction avec le `->`  après le nom de la fonction et les paramètres.

Le modulo `%` est un opérateur qui renvoie le reste d'une division euclidienne.
Donc si on a un nombre `x` et qu'on veut savoir si il est pair, on peut utiliser le modulo pour savoir si le reste de sa division par 2 est 0.

On peut maintenant utiliser la fonction `isEven` pour afficher les nombres pairs de 1 à 10:
```rust
fn main() {
    for i in 1..11 {
        if is_even(i) {
            println!("{} est pair", i);
        }
    }
}
```
Sortie:
```
2 est pair
4 est pair
6 est pair
8 est pair
10 est pair
```


---

<p align="right"><a href="../les-blocs-de-code">Section suivante ⏭️</a></p>

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>