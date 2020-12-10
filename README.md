# Maximális megtakarítás kiszámítása

## Feladat

Szeretnénk nyomon követni több héten keresztül, hogy mennyi pénzt tudunk legjobb esetben félretenni, ha
`K` adott nap megtakarítását vehetjük figyelembe.
Egy szabály van: ha egy adott napra vonatkozó megtakarítást be szeretnénk választani a „legjobbak” közé,
akkor annak a hétnek minden előtte levő napját figyelembe kell vegyük az összeg kiszámításakor.


Határozzuk meg a `K` napra vonatkozó maximális megtakaritás értékét, ha betartjuk a fenti szabályt. 

## Bemenet

A bemenet első sora a hetek `N` és a napok `M` számát tartalmazza 
  - ahol `N` és `M` 2 és 100 közötti természetes számok.

A bemenet következő sorától kezdődően egy `NXM` méretű mátrix `A` elemei következnek. 
  - az `A` mátrix `i` sora és `j` oszlopa által meghatározott cella azt mondja meg, hogy az `i`. hét `j`. napján mennyi volt a megtakarított pénzem.
  
A bemenet utolsó sorában egy `K` érték van, amely azon napok számát jelöli, ahány napra vonatkozóan ki szeretném számolni a maximális megtakarítás összértékét.

## Kimenet

A program egy természetes számot kell kiírjon, amely a K napra vonatkozó megtakarítások összértékét jelöli.


## Példák

### Példa 1

Bemenet:
```
2 4
10 10 100 30
80 50 10 50
3
```

Kimenet:
```
140
```

Kiválasztjuk az első hét első napját (10) és a második hét első két napját (80, 50). 10 + 80 + 50 = 140

### Példa 2

Bemenet:
```
2 4
10 10 100 30
80 50 10 50
5
```

Kimenet:
```
250
```

Kiválasztjuk az első hét első három napját (10, 10, 100) és a második hét első két napját (80, 50). 10 + 10 + 100 + 80 + 50 = 250

### Példa 3

Bemenet:
```
3 4
30 10 110 13
810 152 12 5
124 24 54 124
6
```

Output:
```
1288
```

Kiválasztjuk a második hét első két napját (810, 152) és a harmadik hétnek mind a négy napját (124, 24, 54, 124). 810 + 152 + 124 + 24 + 54 + 124 = 1288

