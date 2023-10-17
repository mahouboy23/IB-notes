---
tags : mod cs
---
Created: 2023-10-17

Ex1:
```python
input a
input b
if a < b then
  output "le nombre le plus grand est ", b
elif a > b then
  output "Le nombre le plus grand est", a
else a = b then 
  output a, "est egal a", b
end if
```


Ex2:
1. Un diagramme de GANTT est un type de diagramme qui utilise des barre et est utiliser pour la planification des taches dans un projects. Sa spécialité est qu'il permet de visualiser les taches d'un project dans un diagramme a barre durant un période ce qui permet d'organiser les taches et de les simultanément, successivement ou attendre un tache de finir avant de commencer une autre.

2. La recherche séquentielle: commence par comparer la valeur du premier element a la valeur qu'on cherche si c'est egal on a trouver la valeur sinon on doit continuer au prochain element du tableau pour comparer et continu ce processus jusqu'à on trouve l'element ou on fini la liste 
   la recherche binaire: commence par trouver l'element median de la liste et regarder si l'element qu'on cherche est supérieur, inferieur ou egal a la valeur de l'eleman median, si elle est egal on a trouver le nombre si non on prend la partie supérieur ou inferieur des elements de la liste et on trouve la median de cette parie et on recommence le processus jusqu'à on trouve le nombre.
   Le tri a bulles: commence par prendre la valeur du premier element et le comparer a la valeur du deuxième si elle est supérieur on inferieur soit on échange les valeurs des deux element soit on ne change rien de meme si elle sont égaux (depends de si on l'ordonne par ordre croissant ou décroissant). Puis après on prend la valeur prochain du prochain element et on la compare celle du deuxièmes element et ainsi de suite jusqu'à qu'on ordonne toute la liste.

3. Les languages de haut niveau doit être traduit car le language de haut utilise le vocabulaire (syntax) humain mais le machine ne pas utiliser et comprendre se language donc on doit traduit le languages de haut niveau on language que la machine peut comprendre pour qu'il puisse executer le code.

4. La traduction d'une language de haut en code executable se fait en en traduisant le language de haut niveau en utilisant un interpréteur qui traduit en code source ou l'ordinatuer peut lire et comprendre puis execute le code ligne par ligne ou un compiler qui traduit en code source ou l'ordinatuer peut lire et comprendre tout le code d'abord puis execute le code.
Ex 3:
![[image-20231017115158258.png]]

Ex 4:
a) Non il n'est pas correct
b) il faut changer le FOUND = TRUE a FOUND =FALSE

Ex 5:
a) $101101_{2} = 2^{0}+2^{2}+2^{3}+2^{5} = 45_{10}$
b) $55_{10} = 2^0+2^1+2^{2}+2^{4}+2^{5} = 110111_{2}$ 

Ex 6:
1. a) ![[Drawing 2023-10-17 11.12.33.excalidraw]]
   b) ![[Drawing 2023-10-17 11.21.13.excalidraw]]
2. a) 
![[image-20231017113432760.png]]
   b)
![[image-20231017113451896.png]]

Ex 7:
```python
NOTES = new(Collection)
NOTES.resetnext()
MAX = NOTES.getNext()
MIN = MAX
TOTAL = 0
B = 0
MEAN = 0
VAL = 0
mq
reset.next()
loop while NOTES.hasNext()
 VAL = NOTES.getNext()
 B = B + 1
 TOTAL = TOTAL + VAL
 if VAL > MAX then
  MAX = VAL
 end if
 if VAL < MIN then
  MIN = VAL
 end if
end loop
MEAN = TOTAL/B
output MEAN
output MAX
output MIN
```