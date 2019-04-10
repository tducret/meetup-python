---

# Decorators and iterators in the wild

## Nicola Luminari & Thibault Ducret

---

# Les décorateurs

---

# A quoi ça sert?

<span style="font-size: 18pt">Un décorateur permet de modifier le fonctionnement d'une fonction, d'une méthode ou d'une classe, **sans modifier son code source**.</span>


<span style="font-size: 14pt; font-style: italic">Le décorateur est un des 23 patrons de conception du livre **Design Patterns** :arrow_right:</span>

{.column}

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/design_patterns.jpg)


---

# Prenons un exemple

![](https://images.pexels.com/photos/821653/pexels-photo-821653.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260)


{.column}

```python {style="font-size: 24pt"}
def prendre_photo():
    photo = click()
    return photo
```

---

# Un décorateur peut modifier le nombre d'exécutions d'une fonction

![](https://images.pexels.com/photos/1500590/pexels-photo-1500590.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260)

{.column}

```python {style="font-size: 20pt"}
def prendre_photo():
    photo = click()
    return photo

prendre_photo = timelapse(prendre_photo)
```

---

# Un décorateur peut modifier le nombre d'exécutions d'une fonction

![](https://images.pexels.com/photos/1500590/pexels-photo-1500590.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260)

{.column}

```python {style="font-size: 20pt"}
def prendre_photo():
    photo = click()
    return photo

prendre_photo = timelapse(prendre_photo)
```

**Et avec un peu de sucre syntaxique?**

---

# Un décorateur peut modifier le nombre d'exécutions d'une fonction

![](https://images.pexels.com/photos/1500590/pexels-photo-1500590.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260)

{.column}

```python {style="font-size: 20pt"}
@timelapse
def prendre_photo():
    photo = click()
    return photo
```

---

# Un décorateur peut modifier la sortie de la fonction

![](https://images.pexels.com/photos/403495/pexels-photo-403495.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260)

{.column}

```python {style="font-size: 20pt"}
@noir_et_blanc
def prendre_photo():
    photo = click()
    return photo
```

---

# Un décorateur peut ajouter de nouvelles fonctionnalités

![](https://media.giphy.com/media/WoRag9vPhr5f5Ef2ng/giphy.gif)

{.column}

```python {style="font-size: 20pt"}
@peut_voler
def prendre_photo():
    photo = click()
    return photo
```

**:warning: Cette slide peut contenir un placement de produit...**

---

# Récapitulatif

## Un décorateur peut :

- Modifier **le nombre d'exécutions** d'une fonction
- Modifier **sa sortie** *(et même **ses entrées**)*
- **Étendre** ses fonctionnalités


---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/valerie_damidot_bulle.jpg){.background}

---

# DEMO :boom:

## sur [repl.it](https://repl.it/@tducret/deco)

---

# Liens vers les exemples de code

- [@repeat](https://repl.it/@tducret/deco1) : modifier le nombre d'exécutions d'une fonction
- [@uppercase](https://repl.it/@tducret/deco2) : modifier la valeur de sortie d'une fonction
- [@reverse_name](https://repl.it/@tducret/deco3) : modifier les entrées d'une fonction
- [@chrono](https://repl.it/@tducret/deco4) : chronométrer l'exécution d'une fonction
- [@slow_down](https://repl.it/@tducret/deco5) : ralentir l'exécution d'une fonction
- [@trace](https://repl.it/@tducret/deco6) : tracer les entrées et sorties d'une fonction
- [@repeat(num_times)](https://repl.it/@tducret/deco7) : modifier le nombre d'exécutions d'une fonction (version paramétrable)
- [@count_executions + @lru_cache](https://repl.it/@tducret/deco8) : compter le nombre d'exécutions d'une fonction (décorateur à état)

---

# Modifier le nombre d'exécutions d'une fonction

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

# Modifier le nombre d'exécutions d'une fonction *(paramétrable)*

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco7.png){.background}

---

# Compter le nombre d'exécutions *(décorateur à état)*

---

![](https://github.com/tducret/meetup-python/raw/master/2019.04.11_Decorators_and_iterators_in_the_wild/Images/deco8.png){.background}

---