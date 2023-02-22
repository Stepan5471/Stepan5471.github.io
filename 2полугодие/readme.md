# Dillinger
## _The Last Markdown Editor, Ever_

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

| № | status |
| - | - |
|1| |
|2| |
|3| |
|4| |
|5|+|
|6| |
|7| |
|8| |
|9| |
|10| |
|11| |
|12| |
|13| |
|14| |
|15| |
|16| |
|17| |
|18| |
|19| |
|20| |
|21| |
|22| |
|23| |
|24| |
|25| |
|26| |
|27| |

Исходные коды (методы решения):

5) 

1. Организовать цикл перебора чисел

2. Перевод числа в 2-ю СС (bin , f'{n:b}')

3. Выполнение условий задачи с дописью и заменой.

4. Перевод в int и проверка на условие

5. После вывода минимального, прерывание break

for i in range(1,100):

chislo=''

num=(bin(i)[2:])

if num.count('1')%2==0:

chislo='10'+num[2:]+'0'


if num.count('1')%2!=0:

chislo='11'+num[2:]+'1'

if int(chislo,2)>40:

print (i, int(chislo,2))

break

6) задание с черепашкой

1. Вспомнить команды черепашки

2. Воспроизвести алгоритм задачи

3. Расставить сами точки внутри контура

4. Вручную посчитать точки
(жирность точек не влияет на подсчет)

left(90)

for i in range(7):

forward(300)

right(120)

pu()

for x in range(1,9):

for y in range(1,10):

goto(x*30,y*30)

dot(5)

done()

27 задание:
with open('27-B.txt') as f:
    c = [int(x) for x in f]
    c.pop(0)

l=len(c)

summ = []
start = 0
step = 50000
x = len(c) // step
zn = []
c = c + c
for i in range(x):
    su=0
    a = c[start+i*step:start+i*step + l]
    # для первого(нулевого)
    for ii in range(len(a)):
        if ii > len(a) // 2:nomer = len(a) - ii
        else:nomer = ii - 0
        su=su+a[ii] * nomer
    summ.append(su)
    zn.append(start+i*step)

n=0
for i in summ:
    nn=step*n
    print(start+nn,i)
    n=n+1
print(min(summ),zn[summ.index(min(summ))]+1)

start = zn[summ.index(min(summ))]-step//2
finish=zn[summ.index(min(summ))]+step//2

step = 10000
while True:
    step = step // 4
    if step==0:step=1
    i = 0
    print(start, finish, step)
    input('Продолжаем')
    posit = start
    zn = []
    summ = []

    while posit<= finish:
        i+=1
        su = 0
        a = c[start+i*step:start+i*step + l]
        # для первого(нулевого)
        for ii in range(len(a)):
            if ii > len(a) // 2:nomer = len(a) - ii
            else:nomer = ii - 0
            su=su+a[ii] * nomer
        summ.append(su)
        zn.append(start+i*step)
        posit+=step
    n=0
    for i in summ:
        nn=step*n
        print(start+nn,i)
        n=n+1
    print(min(summ),zn[summ.index(min(summ))]+1)
    start = zn[summ.index(min(summ))] - step*2
    finish = zn[summ.index(min(summ))] + step*2
