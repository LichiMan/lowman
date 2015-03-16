# Creature #

Un _creature_ es un _transform node_ con unos determinados atributos que la definen. Su nombre es el de la criatura.

## Attributes ##

  * **creature** : Un _string_ con el nombre de la criatura.
  * **creatureType** : Un _enum_ con el tipo de criatura como _biped_, _quadruped_, etc.
  * **creatureStatus** : Un _enum_ con tres opciones: _low_, _medium_, _full_.
  * **creatureObjects** : Un _message_ en el que se connectan los diferentes objetos que componen la criatura para futuras transferencias de animación, etc.

## Jerarquía ##

El _creature_ tiene la siguiente jerarquía:

```
creature
   |_ creature_placement
   |_ creature_joints
   |_ creature_geometry
   |_ creature_constraints
   |_ creature_clusters
   |_ creature_extras
```

### creature\_placement ###

El _shape_ de _`creature_placement`_ es un _nurbsCurve_ con forma de círculo con cuatro flechas:

`curve -d 1 -p 1 0 -3.869373 -p 1.171566 0 -3.824357 -p 1.508784 0 -3.71192 -p 1.988757 0 -3.479641 -p 2.434536 0 -3.187017 -p 2.837254 0 -2.837254 -p 3.187017 0 -2.434536 -p 3.479641 0 -1.988757 -p 3.71192 0 -1.508784 -p 3.824357 0 -1.171566 -p 3.869373 0 -1 -p 5 0 -1 -p 6 0 -1 -p 6 0 -2 -p 8 0 0 -p 6 0 2 -p 6 0 1 -p 5 0 1 -p 3.869373 0 1 -p 3.824357 0 1.171566 -p 3.71192 0 1.508784 -p 3.479641 0 1.988757 -p 3.187017 0 2.434536 -p 2.837254 0 2.837254 -p 2.434536 0 3.187017 -p 1.988757 0 3.479641 -p 1.508784 0 3.71192 -p 1.171566 0 3.824357 -p 1 0 3.869373 -p 1 0 5 -p 1 -1 5 -p 2 -1 5 -p 0 -3 5 -p -2 -1 5 -p -1 -1 5 -p -1 0 5 -p -1 0 3.869373 -p -1.171566 0 3.824357 -p -1.508784 0 3.71192 -p -1.988757 0 3.479641 -p -2.434536 0 3.187017 -p -2.837254 0 2.837254 -p -3.187017 0 2.434536 -p -3.479641 0 1.988757 -p -3.71192 0 1.508784 -p -3.824357 0 1.171566 -p -3.869373 0 1 -p -5 0 1 -p -6 0 1 -p -6 0 2 -p -8 0 0 -p -6 0 -2 -p -6 0 -1 -p -5 0 -1 -p -3.869373 0 -1 -p -3.824357 0 -1.171566 -p -3.71192 0 -1.508784 -p -3.479641 0 -1.988757 -p -3.187017 0 -2.434536 -p -2.837254 0 -2.837254 -p -2.434536 0 -3.187017 -p -1.988757 0 -3.479641 -p -1.508784 0 -3.71192 -p -1.171566 0 -3.824357 -p -1 0 -3.869373 -p -1 0 -5 -p -1 1 -5 -p -2 1 -5 -p 0 3 -5 -p 2 1 -5 -p 1 1 -5 -p 1 0 -5 -p 1 0 -3.869373 -k 0 -k 1 -k 2 -k 3 -k 4 -k 5 -k 6 -k 7 -k 8 -k 9 -k 10 -k 11 -k 12 -k 13 -k 14 -k 15 -k 16 -k 17 -k 18 -k 19 -k 20 -k 21 -k 22 -k 23 -k 24 -k 25 -k 26 -k 27 -k 28 -k 29 -k 30 -k 31 -k 32 -k 33 -k 34 -k 35 -k 36 -k 37 -k 38 -k 39 -k 40 -k 41 -k 42 -k 43 -k 44 -k 45 -k 46 -k 47 -k 48 -k 49 -k 50 -k 51 -k 52 -k 53 -k 54 -k 55 -k 56 -k 57 -k 58 -k 59 -k 60 -k 61 -k 62 -k 63 -k 64 -k 65 -k 66 -k 67 -k 68 -k 69 -k 70 -k 71 -k 72 ;`

Los siguientes atributos solo están en el _creatureStatus low_:
  * **scaleGuides** : Un _float_ al que están conectados todos los _`GuideImplicitSphereShape.radius`_.
  * **scaleAims** : Un _float_ al que están conectados todos los _`GuideUpObjectShape.localScale`_.