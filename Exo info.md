---
tags : mod cs
---
Created: 2023-06-07

Ex 1: 
``` python
N1 = input("Saisir le 1er nombre ")
N2 = input("Saisir le 2eme nombre ")
output N1 * N2
```

Ex 2:
``` java
Nombre = input("Donner un nombre")
if Nombre != 5 and Nombre != 6 then
    output "C'est ni un 5 ni un 6"
end if
```

Ex 3: 



ex 4: 
``` python
A = 0
B = 0
loop A from 1 to 20 
 B = B + 5
 output B
```

ex 5:
```python
A = 0
B = input("Donner le point d'arret")
loop A from 0 to B
 if A mod 2 = 0 then
  output A
 end if
end loop
```

ex 6:
```python 
A = new Array()
B = 0
S = 0
average = 0
min = A[0]
max = A[0]


loop B from 0 to 4
 A[B] = input("Donner un nombre")
end loop

loop B from 0 to 4
 output "Array position", B, "contient la valeur", A[B]
end loop

loop B from 0 to 4
 if min >= A[B] then
  min = A[B]
 end if
 if max <= A[B] then
  max = A[B]
 end if
 S = S + A[B]
end loop

average = S/5

output "Average = ", Average, "max = " , max, "min = ", min 
```

ex 7:
```python
input_string = input("Enter a list element separated by space ")
list1  = input_string.split()
def bubble_sort(list1):  
    has_swapped = True  
    while(has_swapped):  
        has_swapped = False  
        for i in range(len(list1) - 1):  
            if list1[i] > list1[i+1]:  
                list1[i], list1[i+1] = list1[i+1], list1[i]  
                has_swapped = True  
    return list1

print("The unsorted list is: ", list1)  

print("The sorted list is: ", bubble_sort(list1))
```
