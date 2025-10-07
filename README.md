# py_lab1.2
# Лабораторная работа 1.2 Написание скриптов с использованием условных операторов. Решение задач с использованием циклов
## Цели:
- Изучить основные управляющие конструкции языка Python: условный
оператор и циклы.
- Научиться использовать управляющие структуры для решения задач
различной сложности.
- Закрепить навыки обработки данных с использованием коллекций и
итераторов.
- Развить умение комбинировать условия и циклы для оптимизации
алгоритмов.
## Задачи:
- Освоить условный оператор if-elif-else и научиться применять его для
решения задач с разветвлением логики.
- Понять работу циклов while и for, включая их особенности.
- Изучить методы работы с коллекциями в циклах (например, списки, словари,
множества).
- Разобраться с командами управления циклами break и continue.
- Изучить коллекционные включения (list comprehensions) для создания новых
коллекций.
- Практически применять комбинации условий и циклов для построения
сложных алгоритмов

# Выполнение заданий
## Условный цикл
## № 1.2.1

<img width="724" height="180" alt="image" src="https://github.com/user-attachments/assets/c4f1338f-fc85-49c3-8ef4-c5f4d2d840af" />

Решение
````
x = int(input("Введите х: "))

if x >= 0:
    f = x**(1/2) + x**2
else:
    f = 1 / x
print(round(f))
````
Результат выолнения

<img width="319" height="224" alt="image" src="https://github.com/user-attachments/assets/1bc48c9f-648a-4120-9cd6-5b8eaf975cc4" />

## № 1.2.2 Определите максимальное и минимальное значения из двух различных целых чисел.
Решение 
````
x=int(input("Введите значение х: "))
y=int(input("Введите значение у: "))

if x>y:
  mini=y
  maxi=x
else:
  mini=x
  maxi=y

print(f"Минимальное число - {mini}, максимальное число - {maxi}")
````
Результат выполнения

<img width="617" height="324" alt="image" src="https://github.com/user-attachments/assets/097ccb2d-cb8e-4c4e-b809-fb837283cfce" />

## № 1.2.3
Вася пытается высунуть голову в форточку размерами a и b см. Приняв условно,
что его голова - круглая диаметром d см, определите, сможет ли Вася сделать это.
Для прохождения головы в форточку необходим зазор в 1 см. с каждой стороны.
Все величины - целые числа.

Решение 
````
a=int(input("Введите сторону а: "))
b=int(input("Введите сторону b: "))
d=int(input("Введите диаметр: "))

a_zazor = a - 2
b_zazor = b - 2

if d <= a_zazor and d <= b_zazor:
    print("Да, получится")
else:
    print("Нет, не получится")
````
Результат выполнения

<img width="398" height="338" alt="image" src="https://github.com/user-attachments/assets/66c60a02-b55c-406a-8ec7-edb1b7a9749f" />

## № 1.2.4 Известны год и номер месяца сегодняшнего дня, а также год и номер месяца рождения человека (нумерация месяцев с 1: январь - 1 и т.д.). Определите возраст человека (число полных лет).

Решение

````
year_today = 2025
month_today = 9

year = int(input("Введите год рождения: "))
month = int(input("Введите месяц рождения: "))

if month <= month_today:
  age= year_today - year
else:
  age= year_today - year - 1


print("Число полных лет: ", age)
````
Результат выполнения

<img width="440" height="360" alt="image" src="https://github.com/user-attachments/assets/99ea1ae8-14db-4718-b8ed-dc439cc094ea" />

## № 1.2.5 Дана точка с целыми ненулевыми координатами (x;y). Определить номер четверти координатной плоскости, которой она принадлежит.

Решение

````
x=int(input("Задайте х: "))
y=int(input("Задайте у: "))

if x>0 and y>0:
  print("Первая четверть")
elif x<0 and y>o:
  print("Вторая четверть")
elif x<0 and y<0:
  print("Третья четверть")
else:
  print("Четвертая четверть")
````
Результат выполнения

<img width="329" height="346" alt="image" src="https://github.com/user-attachments/assets/c687e919-7a6c-46d3-b142-7c18976cd5ff" />

## № 1.2.6 Даны вещественные числа a, b, c (a≠0). Решите уравнение ax2+bx+c=0. При выводе значений оставьте 1 знак после запятой.

Решение

````
a=float(input("Введите число а: "))
b=float(input("Введите число b: "))
c=float(input("Введите число с: "))

D= b**2 - 4*a*c

if D>0:
  x1= (-b + D **(1/2))/ (2*a)
  x2= (-b - D **(1/2))/ (2*a)
  print(round(x1,1), round(x2, 1))
else:
  print("Корней нет")
````
Результат выполнения

<img width="411" height="361" alt="image" src="https://github.com/user-attachments/assets/b0de05ff-4399-4418-99dc-2ffaeaf5e408" />

## Цикл с условием
## № 1.2.7 Дана непустая последовательность целых чисел, оканчивающаяся нулем. Найти сумму и количество введенных чисел.

Решение

````
nums_sum = 0
nums_count = 0

x = int(input("Введите число: "))

while x != 0:
    nums_sum += x
    nums_count += 1
    x = int(input("Введите число: "))

print("Сумма =", nums_sum)
print("Количество =", nums_count)
````
Результат выполнения

<img width="391" height="425" alt="image" src="https://github.com/user-attachments/assets/59dbe007-76c3-4591-b429-fa293d128246" />

## № 1.2.8 Дано число n. Из чисел 0,5,10,15,20,25,... напечатать те, которые не превышают n.

Решение

````
n = int(input("Введите число n: "))
x = 0
while x <= n:
    print(x)
    x += 5
````
Результат выполнения

<img width="398" height="191" alt="image" src="https://github.com/user-attachments/assets/db6c81a1-1983-4923-871a-0d453b8d2e0d" />


## № 1.2.9 
<img width="840" height="187" alt="image" src="https://github.com/user-attachments/assets/030f37a0-4397-4b5d-a887-fcc7dc450c5f" />


Решение

````
a = float(input("Введите число а: "))
n = 1
x_sum = 0.0

while x_sum <= a:
    x_sum += 1 / n
    n += 1

n -= 1
print(n)
````
Результат выполнения
<img width="389" height="275" alt="image" src="https://github.com/user-attachments/assets/ba4ebf15-6545-42f9-bb7c-f8cd7a57be5c" />


## № 1.2.10 Дано натуральное число. Определите сумму и количество его цифр
Решение
````
n = int(input("Введите число n: "))
n_sum = 0
n_count = 0
a = n

while a > 0:
    cifr = a % 10
    n_sum += cifr
    n_count += 1
    a = a // 10

print("Сумма цифр: ", n_sum)
print("Количество цифр: ", n_count)
````

Результат выполнения

<img width="422" height="367" alt="image" src="https://github.com/user-attachments/assets/6273dbe4-897f-4dfb-80ff-0b631ac8102a" />


## № 1.2.11 Вывести в строку 10 первых натуральных чисел, оканчивающихся на цифру k, кратных числу s и находящихся в интервале, левая граница которого равна start.
Решение
````
start = int(input("Задайте левую границу интервала: "))
k = int(input("Введите число k: "))
s = int(input("Введите сило s: "))
n_count = 0
x = start

while n_count < 10:


    if x % s == 0 and x % 10 == k:
        print(x, end=' ')
        n_count += 1
    x += 1
````

Результат выполнения

<img width="522" height="384" alt="image" src="https://github.com/user-attachments/assets/ada72f02-2a6b-4217-a0b5-2a80d5350bdd" />

## Совместный цикл (цикл по коллекциям)
## № 1.2.12 Даны целые числа a и b (a может быть больше b). Напечатайте:  числа от минимального до максимального в строчку (разделяя пробелом);  числа от максимального до минимального «столбиком».
Решение
````
a= int(input())
b= int(input())

low=min(a,b)
high=max(a,b)

n_count = 0
num = start

for i in range(low, high + 1):
    print(i, end=" ")
print()

for i in range(high, low - 1, -1):
    print(i)
````

Результат выполнения

<img width="424" height="539" alt="image" src="https://github.com/user-attachments/assets/20dafd96-caec-464c-84b6-5b3357a13c87" />


## № 1.2.13 Для введенных с клавиатуры положительных целых чисел a и b (a≤b) определите:  сумму всех целых чисел от a до b;  произведение всех целых чисел от a до b;  среднее арифметическое всех целых чисел от a до b;  среднее геометрическое нечетных чисел от a до b. Отрезок поиска включает сами числа a и b. При выводе вещественных результатов оставьте два знака после запятой.
Решение
````
a = int(input("a = "))
b = int(input("b = "))

n_sum = 0
n_mult = 1
nechet_mult = 1
nechet_count = 0
count = 0

for i in range(a, b + 1):
    n_sum += i
    n_mult *= i
    count += 1
    if i % 2 != 0:
        nechet_mult *= i
        nechet_count += 1

n_avg = n_sum / count

if nechet_count > 0:
    n_avg_geom = nechet_mult ** (1 / nechet_count)
else:
    n_avg_geom = 0

print("Сумма =", n_sum)
print("Произведение =", n_mult)
print("Среднее арифметическое = {:.2f}".format(n_avg))
print("Среднее геометрическое нечетных чисел = {:.2f}".format(n_avg_geom))
````

Результат выполнения

<img width="462" height="133" alt="image" src="https://github.com/user-attachments/assets/c25798ef-f923-4e0f-ade4-86fd60292945" />


## № 1.2.14 Начав тренировки, лыжник в первый день пробежал s км. (s>0, вещественное число). Каждый следующий день он увеличивал пробег на p % (0<p≤100, вещественное число) от пробега предыдущего дня. Определите:  пробег лыжника за второй, третий, …, десятый день тренировок;  какой суммарный путь он пробежал за первые 10 дней тренировок. При выводе вещественных результатов оставьте один знак после запятой.
Решение
````
s = float(input("Пробег за 1-й день в км): "))
p = float(input("На сколько увеличивает пробег в %: "))

all_pr = s

for day in range(2, 11):
    s = s + s * p / 100
    all_pr += s
    print(f"Пробег за {day}-й день: {s:.1f} км.")

print("Суммарный пробег: {:.1f} км.".format(all_pr))
````

Результат выполнения

<img width="390" height="243" alt="image" src="https://github.com/user-attachments/assets/77829b62-605f-4752-9edd-3e6fd4839ec3" />


## № 1.2.15 Известна масса каждого предмета в кг., загружаемого в грузовик. Определить, возможна ли перевозка груза, если грузоподъемность грузовика равна p кг.
Решение
````
p = float(input("Грузоподъемность грузовика в кг: "))
n = int(input("Количество предметов: "))

m = 0

for i in range(1, n + 1):
    mass = float(input(f"Масса {i}-го предмета в кг: "))
    m += mass

if m <= p:
    print("Да")
else:
    print("Нет")
````

Результат выполнения

<img width="342" height="113" alt="image" src="https://github.com/user-attachments/assets/28692aef-b490-49fe-ab0e-7e7e73fb14a1" />


## № 1.2.16 В области несколько районов. Заданы площади, засеваемые пшеницей (га.), и средняя урожайность (ц/га) в каждом районе. Определите количество пшеницы, собранное по области. При выводе вещественных результатов оставьте один знак после запятой.
Решение
````
n = int(input("Количество районов: "))

m = 0.0

for i in range(1, n + 1):
    area = float(input(f"Площадь {i}-го района в га:  "))
    yield_avg = float(input(f"Урожайность в {i}-м районе в ц/га: "))
    m += area * yield_avg

print("Собрано пшеницы: {:.1f} ц.".format(m))
````

Результат выполнения

<img width="344" height="171" alt="image" src="https://github.com/user-attachments/assets/81b96313-8c9f-4c55-8c00-9e2199a8bb45" />

##  Прерывание и продолжение циклов
## № 1.2.17 Решите задачу № 2.7, организовав бесконечный цикл, который бы прерывался при выполнении условия, используя оператор break 
Решение
````
nums_sum = 0
nums_count = 0
i = 1

while True:
    x = int(input(f"Введите {i}-е число: "))
    if x == 0:
        break
    nums_sum += x
    nums_count += 1
    i += 1

print("Сумма: ", nums_sum)
print("Количество: ", nums_count)
````

Результат выполнения

<img width="259" height="129" alt="image" src="https://github.com/user-attachments/assets/e92edb6c-2bdf-4004-8b0c-164c5b44fdc0" />

## № 1.2.18 Предложение, введенное с клавиатуры, содержит слова из гласных и согласных букв кириллицы (регистр может быть различный), а также пробелы. Определите количество гласных и согласных букв в предложении. Для пропуска пробелов используйте оператор continue .
Решение
````
sentence = input("Введите предложение: ")

gl = 0
sogl = 0

gllow = "аеёиоуыэюя"

for ch in sentence:
    ch = ch.lower()
    if ch == " ":
        continue
    if ch in gllow:
        gl += 1
    else:
        sogl += 1

print(f"Количество букв в предложении: гласных - {gl}, согласных - {sogl}")
````

Результат выполнения

<img width="531" height="55" alt="image" src="https://github.com/user-attachments/assets/9bd7f43c-a0c7-4d50-a41a-da704cd81bce" />

##  Комбинация циклов и условий
## № 1.2.19 Выведите на экран (в строку) все целые числа от a до b, кратные некоторому числу c
Решение
````
a = int(input("Введите число a: "))
b = int(input("Введите число b: "))
c = int(input("Введите число c: "))

for i in range(a, b + 1):
    if i % c == 0:
        print(i, end=" ")
````

Результат выполнения

<img width="240" height="91" alt="image" src="https://github.com/user-attachments/assets/67489993-ab1b-442b-a5b3-e6af07d72348" />

## № 1.2.20 Выведите на экран (в строку) все трехзначные натуральные числа, сумма цифр которых равна целому числу n (0<n≤27).
Решение
````
n = int(input("Введите число n: "))

for digit in range(100, 1000):
    sotka = digit // 100
    ten = (digit // 10) % 10
    edin = digit % 10

    if sotka + ten + edin == n:
        print(digit, end=" ")
````

Результат выполнения

<img width="248" height="45" alt="image" src="https://github.com/user-attachments/assets/529b4b82-d6ce-4611-afd8-409d1299e9ba" />

## № 1.2.21 Известно количество учеников в классе и их рост (см.); рост мальчиков условно задан отрицательными числами. Определите средний рост мальчиков и средний рост девочек. При выводе вещественных результатов оставьте один знак после запятой.
Решение
````
n = int(input("Введите число n: "))

rost_boys = 0.0
count_boys = 0
rost_girls = 0.0
count_girls = 0

for i in range(1, n + 1):
    r = int(input(f"Рост {i}-го ученика: "))
    if r < 0:
        rost_boys += abs(r)
        count_boys += 1
    else:
        rost_girls += r
        count_girls += 1

r_sr_m = rost_boys / count_boys if count_boys > 0 else 0
r_sr_d = rost_girls / count_girls if count_girls > 0 else 0

print("Средний рост мальчиков: {:.1f}".format(r_sr_m))
print("Средний рост девочек: {:.1f}".format(r_sr_d))
````
Результат выполнения

<img width="300" height="162" alt="image" src="https://github.com/user-attachments/assets/c968aaa1-63a6-4003-991e-a64b5c2230d4" />

## № 1.2.22 Даны n вещественных чисел. Определите максимальное и минимальное из них. При выводе вещественных результатов оставьте два знака после запятой.
Решение
````
n = int(input("Введите число n: "))

a_max = None
a_min = None

for i in range(1, n + 1):
    x = float(input(f"{i}-е число:  "))
    if a_min is None or x < a_min:
        a_min = x
    if a_max is None or x > a_max:
        a_max = x

print("Максимальное число: {:.2f}".format(a_max))
print("Минимальное число: {:.2f}".format(a_min))
````
Результат выполнения

<img width="245" height="96" alt="image" src="https://github.com/user-attachments/assets/0c82a85c-4885-4870-b5e3-e188973dfe14" />

## № 1.2.23 Дано натуральное число n. Определите, является ли оно членом последовательности Фибоначчи .
Решение
````
n = int(input("Введите число n: "))
a, b = 0, 1
fibonachi = False

while b <= n:
    if b == n:
        fibonachi = True
        break
    a, b = b, a + b

print("Является" if fibonachi else "Не является")
````
Результат выполнения

<img width="218" height="52" alt="image" src="https://github.com/user-attachments/assets/75da7590-19c6-4eab-aa02-9541f49341c6" />

## № 1.2.24 Дано n вещественных чисел. Определите, является ли последовательность упорядоченной по возрастанию. В случае отрицательного ответа выведите порядковый номер числа, нарушающего такую упорядоченность.
Решение
````
n = int(input("Введите число n: "))
if n <= 1:
    print("Последовательность является упорядоченной по возрастанию")
else:
    pr = float(input("Первое число: "))
    index = -1

    for i in range(2, n + 1):
        c = float(input(f"{i}-е число: "))
        if c <= pr: 
            index = i
            break
        pr = c

    if index == -1:
        print("Последовательность является упорядоченной по возрастанию")
    else:
        print(index)
````
Результат выполнения

<img width="570" height="100" alt="image" src="https://github.com/user-attachments/assets/e74fb336-b227-4244-bed6-aee1b88ca345" />

## № 1.2.25

<img width="642" height="169" alt="image" src="https://github.com/user-attachments/assets/a3bc7b12-8ae7-42d8-8ae5-943b77eb7760" />


Решение
````
n = int(input("Введите число n: "))

for i in range(1, n + 1):
    for j in range(1, n + 1):
        print(f"{i} x {j} = {i * j}", end="   ")
    print()
````
Результат выполнения

<img width="337" height="83" alt="image" src="https://github.com/user-attachments/assets/1276ce73-bae3-4103-b102-a46728075374" />


## № 1.2.26
<img width="853" height="237" alt="image" src="https://github.com/user-attachments/assets/ad26ca8f-096a-4cd9-b2a5-62efe4e6e6e0" />


Решение
````
n = int(input("Введите число n: "))
for num in range(1, n + 1):
    count = 0
    for i in range(1, num + 1):
        if num % i == 0:
            count += 1
    print(num, '*' * count)
````
Результат выполнения

<img width="260" height="104" alt="image" src="https://github.com/user-attachments/assets/e7f14e6d-2d3a-4a49-b13f-fe53e184117f" />

## № 1.2.27 Выведите на экран (в строку) n первых простых чисел.
Решение
````
n = int(input("n = "))  
count = 0   
num = 2
while count < n:
    pr = True
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            pr = False
            break
    if pr:
        print(num, end=" ")
        count += 1
    num += 1

print()
````
Результат выполнения

<img width="232" height="54" alt="image" src="https://github.com/user-attachments/assets/12138f1f-6686-44d4-b8dd-8ae916ca4d24" />

## № 1.2.28 Составьте программу для нахождения всех натуральных решений уравнения x2+y2+z2=k2 , где x,y,z∈[1,30], а k вводится с клавиатуры.
Решение
````
k = int(input())

for x in range(1, 31):
    for y in range(1, 31):
        for z in range(1, 31):
            if x**2 + y**2 + z**2 == k**2:
                print(x, y, z)
````
Результат выполнения

<img width="798" height="670" alt="image" src="https://github.com/user-attachments/assets/4bf911f5-c1de-4f8c-b2ca-966d3b5a8db1" />

## Коллекции
## № 1.2.29 Дан список из n вещественных чисел, введенных с клавиатуры (среди чисел есть по крайней мере одно положительное и отрицательное число). Сформируйте из него 2 списка:  положительных чисел, используя списковые включения;  отрицательных чисел, не используя списковые включения. Выведите на экран:  исходный список;  получившиеся списки;  среднее арифметическое первого списка и среднее геометрическое второго списка. При выводе вещественных результатов оставьте два знака после запятой.
Решение
````
n = int(input())

original = []
for i in range(n):
    num = float(input())
    original.append(num)

positive = [x for x in original if x > 0]

negative = []
for x in original:
    if x < 0:
        negative.append(x)

print(original)
print(positive)
print(negative)

sum_pos = 0.0
count_pos = 0
for x in positive:
    sum_pos += x
    count_pos += 1

avg_arith = sum_pos / count_pos

prod_neg = 1.0
count_neg = 0
for x in negative:
    prod_neg *= abs(x)
    count_neg += 1

avg_geom = prod_neg ** (1.0 / count_neg)

print(f"{avg_arith:.2f}")
print(f"{avg_geom:.2f}")
````
Результат выполнения


<img width="284" height="190" alt="image" src="https://github.com/user-attachments/assets/72a2de7a-4efb-4747-b2ae-e686c41bba03" />

## № 1.2.30 Дан список целых чисел, введенных с клавиатуры (длина неизвестна). Ответьте на вопросы:  являются ли все элементы положительными числами?  есть ли хотя бы один нулевой элемент в списке?  являются ли все элементы четными числами?  есть ли хотя бы один нечетный элемент в списке? Каждый из пунктов выполните дважды: используя стандартный проход в цикле (например, через алгоритм с флажком), и используя функции any() и/или all() .
Решение
````
# Ввод списка целых чисел из одной строки
data = list(map(int, input().split()))

# 1. Все ли элементы положительные?
# цикл с флажком
all_positive_flag = True
for x in data:
    if x <= 0:
        all_positive_flag = False
        break
# all()
all_positive_builtin = all(x > 0 for x in data)

print("1. Все элементы положительные?")
print("  Цикл:", all_positive_flag)
print("  all():", all_positive_builtin)

# 2. Есть ли хотя бы один нулевой элемент?
# цикл с флажком
has_zero_flag = False
for x in data:
    if x == 0:
        has_zero_flag = True
        break
# any()
has_zero_builtin = any(x == 0 for x in data)

print("2. Есть ли хотя бы один ноль?")
print("  Цикл:", has_zero_flag)
print("  any():", has_zero_builtin)

# 3. Все ли элементы чётные?
# цикл с флажком
all_even_flag = True
for x in data:
    if x % 2 != 0:
        all_even_flag = False
        break
# all()
all_even_builtin = all(x % 2 == 0 for x in data)

print("3. Все элементы чётные?")
print("  Цикл:", all_even_flag)
print("  all():", all_even_builtin)

# 4. Есть ли хотя бы один нечётный элемент?
# цикл с флажком
has_odd_flag = False
for x in data:
    if x % 2 != 0:
        has_odd_flag = True
        break
# any()
has_odd_builtin = any(x % 2 != 0 for x in data)

print("4. Есть ли хотя бы один нечётный?")
print("  Цикл:", has_odd_flag)
print("  any():", has_odd_builtin)
````
Результат выполнения


<img width="383" height="265" alt="image" src="https://github.com/user-attachments/assets/248eafdc-e99b-408a-9f2a-d9e434ee8944" />

## № 1.2.31 Дано предложение. Выведите его на экран, удалив из него все слова, содержащие произвольную букву (вводится с клавиатуры).
Решение
````
sentence = input()
letter = input().strip()[0].lower() 
words = sentence.split()
filtered = []
for word in words:
    if letter not in word.lower():
        filtered.append(word)

print(' '.join(filtered))
````
Результат выполнения


<img width="443" height="66" alt="image" src="https://github.com/user-attachments/assets/d637c6b3-9455-4efa-a85b-2bfda68e51b0" />

## № 1.2.32

<img width="856" height="422" alt="image" src="https://github.com/user-attachments/assets/79650b59-ed45-49f0-b9ec-0234de1365f9" />


Решение
````
n = int(input("Введите количество рядов: "))

seats = []
for i in range(n):
    row = [int(x) for x in input(f"Введите ряд {i+1} (0 - свободно, 1 - занято): ").split()]
    seats.append(row)

count = 0
for row in seats:
    for seat in row:
        if seat == 0:
            count += 1
print("Свободных мест: ", count)

n_p, m_p = [int(item) for item in input("Введите ряд и место через пробел: ").split()]

if n_p < 1 or n_p > len(seats):
    print("Такого места нет")
elif m_p < 1 or m_p > len(seats[n_p - 1]):
    print("Такого места нет")
else:
    free = seats[n_p - 1][m_p - 1] == 0
    print("Место свободно: ", free)
````
Результат выполнения


<img width="422" height="155" alt="image" src="https://github.com/user-attachments/assets/0b3388b7-887f-4865-b4ca-621f5624ff8e" />

## № 1.2.33

<img width="881" height="554" alt="image" src="https://github.com/user-attachments/assets/d3275d7f-5925-47d7-bd9a-c058d5df0dd7" />


Решение
````
n = int(input("Введите количество сотрудников: "))

employees = []
for i in range(n):
    emp = input(f"{i+1}-й сотрудник (Фамилия Имя Отчество Пол Стаж): ").split()
    emp[4] = int(emp[4])  
    employees.append(emp)

for emp in employees:
    print(" ".join(map(str, emp)))

sorted_employees = sorted(employees, key=lambda x: x[4])
employee_min = sorted_employees[0]
employee_max = sorted_employees[-1]

print("Cамый \"молодой\":", " ".join(employee_min[:3]))
print("Cамый \"старый\":", " ".join(employee_max[:3]))

men = [emp for emp in employees if emp[3] == "М"]
women = [emp for emp in employees if emp[3] == "Ж"]

k = input("Введите первую букву имени: ").lower()

men_k_count = sum(1 for emp in men if emp[1].lower().startswith(k))
women_k_count = sum(1 for emp in women if emp[1].lower().startswith(k))

if men_k_count > women_k_count:
    print("У мужчин таких имен больше")
elif women_k_count > men_k_count:
    print("У женщин таких имен больше")
else:
    print("Имен поровну у мужчин и женщин")
````
Результат выполнения


<img width="741" height="232" alt="image" src="https://github.com/user-attachments/assets/ab3ae59e-7faf-457c-82ac-484c94937d47" />

## № 1.2.34
<img width="944" height="602" alt="image" src="https://github.com/user-attachments/assets/083aca5e-f53c-4164-a659-17e97e787c2c" />

Решение
````
n = int(input("Введите количество банков: "))

banks = []
for i in range(n):
    data = input(f"{i+1}-й банк (Название Сумма Процент): ").split()
    bank = {
        "name": data[0],
        "initial_sum": int(data[1]),
        "rate": float(data[2])
    }
    banks.append(bank)

# список проверки
for bank in banks:
    print(bank["name"], bank["initial_sum"], bank["rate"])

# мин первоначальная сумма
affordable_bank = min(banks, key=lambda x: x["initial_sum"])
print(f"Наиболее доступный банк: {affordable_bank['name']}, первоначальная сумма: {affordable_bank['initial_sum']:.2f} руб.")

# макс прибыль
profitable_bank = max(banks, key=lambda x: x["initial_sum"] * x["rate"] / 100)
profit = profitable_bank["initial_sum"] * profitable_bank["rate"] / 100
print(f"Наиболее выгодный банк: {profitable_bank['name']}, прибыль: {profit:.2f} руб.")
````
Результат выполнения


<img width="697" height="153" alt="image" src="https://github.com/user-attachments/assets/1ae26f33-13dc-4ac8-bd1d-71ba813dd89b" />

## Выводы
Практические задания позволили не только изучить синтаксис управляющих конструкций Python, но и научиться мыслить алгоритмически, структурировать данные, оптимизировать перебор и гибко комбинировать инструменты языка для решения разнообразных задач — от простого подсчёта цифр до анализа финансовых предложений и текстовой фильтрации. Полученные навыки являются фундаментом для дальнейшего изучения программирования и разработки более сложных приложений.
