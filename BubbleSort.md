# Bubble Sort 

* Açıklama / Description

{6,5,3,1,8,7,2,4} </br>
{**5,6**,3,1,8,7,2,4} -- 5 < 6 -> atla / swap </br>
{5,**3,6**,1,8,7,2,4} -- 3 < 6 -> atla / swap </br>
{5,3,**1,6**,8,7,2,4} -- 1 < 6 -> atla / swap </br>
{5,3,1,**6,8**,7,2,4} -- 8 > 6 -> atlama / no swap </br>
{5,3,1,6,**7,8**,2,4} -- 7 < 8 -> atla / swap </br>
{5,3,1,6,7,**2,8**,4} -- 2 < 8 -> atla / swap </br>
{5,3,1,6,7,2,**4,8**} -- 4 < 8 -> atla / swap </br>

*** Algoritma dzinin ilk elemanından başlar. Bir sonraki eleman ile karşılaştırılır. Sıra sayısı küçük olan eleman büyük ise elemanların yeri değiştirilir. Mesela 2. eleman 3. elemandan büyük ise 3. eleman 2. elemanın, 2. eleman ise 3. elemanın yerine yerleşir. Böylelikle her adımda en büyük sayı dizinin son elamanı haline gelir. ***

## Kod 
``` c
void bubble_sort(long list[], long n)
{
 long c, d, t;
 for (c = 0 ; c < ( n - 1 ); c++)
 {
 for (d = 0 ; d < n - c - 1; d++)
 {
 if (list[d] > list[d+1])
 {
 /* Swapping */
 t = list[d];
 list[d] = list[d+1];
 list[d+1] = t;
 }
 }
 }
}
```
