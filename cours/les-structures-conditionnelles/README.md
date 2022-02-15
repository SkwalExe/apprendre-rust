# Sommaire📚
- [Les operateurs de comparaison](#les-operateurs-de-comparaison)
- [if](#if)
- [else](#else)
- [else if](#else-if)

# Les structures conditionnelles🏗️
## Les operateurs de comparaison
Les operateurs de comparaison sont utilisés pour comparer des valeurs entre elles.

| Opérateur | Description |
| --------- | ----------- |
| == | Egal à |
| != | Différent de |
| < | Inférieur à |
| > | Supérieur à |
| <= | Inférieur ou égal à |
| >= | Supérieur ou égal à |

## if
Imaginons etre un programmeur et avoir a ecire un programme qui dit si la veleure d'une variable `x` est positive
Pour ca, nous llons verifier si `x` est superieur a 0.
Nous pouvons le faire avec le mot clé `if` (`si` en français)

```rust
if x > 0 {
    println!("x est positif");
}
```

le code entre les `{}` sera executé si la condition `x > 0` est vraie et nous verrons `x est positif` dans la console, sinon, il sera ignoré et rien ne se passera.

## else
Imaginons etre un programmeur et devoir ecrire un programme qui dit "bonjour" si la valeure d'une variable `x` est égale a `5` ou "au revoir" si elle ne l'est pas.

Nous allons d'abord verifier si `x` est égale a `5`, et utiliser le mot clé `else` (`sinon en francais) pour executer du code si la condition n'est pas vraie.
```rust
if x == 5 {
    println!("Bonjour");
} else {
    println!("Au revoir");
}
```
Executons le code avec `x = 5` et nous verrons `Bonjour` dans la console, et avec `x = 6` nous verrons `Au revoir`.

## else if 
Il est possible d'avoir plus d'une condition a verifier.
Imaginons etre un programmeur et devoir ecrire un programme qui dit "bonjour" si la valeure d'une variable `x` est égale a `5`, "bonsoir" si elle est égale a `6` ou "au revoir" si elle ne l'est pas.

```rust
if x == 5 {
    println!("Bonjour");
} else if x == 6 {
    println!("Bonsoir");
} else {
    println!("Au revoir");
}
```

executons le code avec `x = 5` et nous verrons `Bonjour` dans la console, et avec `x = 6` nous verrons `Bonsoir`, avec `x = 7` nous verrons `Au revoir` car aucune des condition n'est vraie.

> ℹ️ Nous pouvons ajouter autant de `else if` que nous le souhaitons. Les conditions des `else if` seront testées dans l'ordre apres le `if` principal.


---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-boucles-infinies">Section suivante ⏭️</a></p>


---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>