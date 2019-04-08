---

# Decorators and iterators in the wild

## Nicola Luminari & Thibault Ducret

---

# Les décorateurs

---

# Un décorateur : à quoi ça sert?

> Un décorateur permet de modifier le fonctionnement d'une fonction, d'une méthode ou d'une classe, **sans modifier son code source**.

{.column}

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/design_patterns.jpg)

---

# Que veut-on dire par *décorer* une fonction?

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/design_patterns.jpg)

{.column}

- Modifier le nombre d'exécutions
- Modifier ses entrées
- Modifier sa sortie
- Étendre ses fonctionnalités

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/valerie_damidot_bulle.jpg){.background}

---

# Modifier le nombre d'exécutions d'une fonction

## @repeat

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco1.png){.background}

---

# Modifier la valeur de sortie d'une fonction

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco2.png){.background}

---

# Modifier les entrées d'une fonction

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco3.png){.background}

---

# Chronométrer l'exécution d'une fonction

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco4.png){.background}

---

# Ralentir l'exécution d'une fonction

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco5.png){.background}

---

# Tracer les entrées et sorties d'une fonction

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco6.png){.background}

---

# Modifier le nombre d'exécutions d'une fonction

## Version 2 : **paramétrable**

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco7.png){.background}

---

# Compter le nombre d'exécutions

## Un décorateur à état

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco8.png){.background}

---

# Liens vers les exemples de code

- [@repeat](https://repl.it/@tducret/deco1)
- [@uppercase](https://repl.it/@tducret/deco2)
- [@reverse_name](https://repl.it/@tducret/deco3)
- [@chrono](https://repl.it/@tducret/deco4)
- [@slow_down](https://repl.it/@tducret/deco5)
- [@trace](https://repl.it/@tducret/deco6)
- [@repeat(num_times)](https://repl.it/@tducret/deco7)
- [@count_executions + @lru_cache](https://repl.it/@tducret/deco8)

---