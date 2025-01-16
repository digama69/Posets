# Décomposition en facteurs premiers
### L'objectif est de décomposer en facteurs premiers le nombre de posets à n éléments.

Le posets viens de « **P**artially **O**rdered **sets** », ce sont des éléments étiquetés (cf.posets.pdf).

On défini L en se basant sur la liste de [posets A001035 de l'OEIS](https://oeis.org/A001035).

```
L = [
 1,
 1,
 3,
 19,
 219,
 4231,
 130023,
 6129859,
 431723379,
 44511042511,
 6611065248783,
 1396281677105899,
 414864951055853499,
 171850728381587059351,
 98484324257128207032183,
 77567171020440688353049939,
 83480529785490157813844256579,
 122152541250295322862941281269151,
 241939392597201176602897820148085023
 ]
```
On utilise la fonction *factor* de SageMath qui décompose en facteurs premiers cette liste à n élément où n varie de 1 à 18
```python
for i in [1..18]:
    facteurs_premiers = factor(L[i])
    print(i, facteurs_premiers)
```
Ce qui nous donne ce tableau :
|Rang|Facteurs premiers|
|:---:|---|
|1| 1|
|2| 3|
|3| 19|
|4| 3 * 73|
|5| 4231|
|6| 3^2 * 14447|
|7| 1481 * 4139|
|8| 3 * 1013 * 142061|
|9| 13 * 31 * 110449237|
|10| 3 * 8963 * 245865047|
|11| 17 * 179 * 458850370393|
|12| 3^2 * 157 * 26821 * 10946861363|
|13| 1470829 * 116839366358419|
|14| 3 * 109 * 1361 * 89187421 * 2481176309|
|15| 79 * 1051 * 934217815708254806791|
|16| 3 * 27826843261830052604614752193|
|17| 59 * 7499 * 21067 * 947369 * 58665227 * 235800391|
|18| 3^2 * 19 * 1414850249106439629256712398526813|
```
