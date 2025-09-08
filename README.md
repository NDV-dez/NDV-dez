<h1 align="center">Hi there, I'm <a href="https://daniilshat.ru/" target="_blank">Dmitry</a> 
<img src="https://github.com/blackcater/blackcater/raw/main/images/Hi.gif" height="32"/></h1>
<h3 align="center">Computer science student</h3>
<h3 align="center"><img src="https://media4.giphy.com/media/v1.Y2lkPTZjMDliOTUyeXE3MDN1NXJzeXQ5c2lud2ZjZnlwZzlpeHl0NmNuN3FvNTMxcnhzaSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/VTtANKl0beDFQRLDTh/200w.gif"></h3>

from math import sin, cos
from random import randint, uniform, random

# 4.37. Составить программу, которая уменьшает первое введенное число в два раза, если оно больше второго введенного числа по абсолютной величине.  

num1 = 56
num2 = -24

if (abs(num1) > abs(num2)) and num1 < 0:
    num1 *= 2
else:
    num1 /= 2

# 4.38. Даны два числа. Если квадратный корень из второго числа меньше первого числа, то увеличить второе число в пять раз. 


if num2**(1/2) < num1:
    num2 *= 5

# 4.42. Даны четыре вещественных числа. Определить, сколько из них отрицательных. Оператор цикла не использовать. 

num1 = 2.5
num2 = -0.4
num3 = 4.56
num4 = -2
count_nagative_num = 0


if num1 < 0:
    count_nagative_num += 1
if num2 < 0:
    count_nagative_num += 1
if num3 < 0:
    count_nagative_num += 1
if num4 < 0:
    count_nagative_num += 1


# 4.50. Даны три различных целых числа. Определить, какое из них (первое, второе или третье): 
# а) самое большое; 
# б) самое маленькое; 
# в) является средним (средним назовем число, которое больше наименьшего из данных чисел, но меньше наибольшего).

num1 = 250
num2 = 450
num3 = 350


sum_number = num1 + num2 + num3
max_num = max(num1,num2,num3)
min_num = min(num1,num2,num3)
print(f'Максимальное значение: {max_num}')
print(f'Минимальное значение: {min_num}')
print(f'Среднее значение: {sum_number - max_num - min_num}')


if num1 > num2 and num1 > num3:
    print(num1)
    if num2 > num3:
        print(f'{num2} среднее')
        print(f'{num3} минимальное')
    else:
        print(f'{num3} среднее')
        print(f'{num2} минимальное')
elif num2 > num1 and num2 > num3:
    print(num2)
    if num1 > num3:
        print(f'{num1} среднее')
        print(f'{num3} минимальное')
    else:
        print(f'{num3} среднее')
        print(f'{num1} минимальное')
# elif...

# 4.59. Дано целое число n (1 <= n <= 99), 
# определяющее возраст человека (в годах). Для этого числа напечатать 
# фразу "мне n лет", учитывая, что при некоторых значениях n 
# слово "лет" надо заменить на слово "год" или "года". 

n = int(input('введите возраст'))

if 5 <= n % 10 <= 9 or 11 <= n <= 20:
    print(f'{n} лет')
elif n % 10 == 1:
    print(f'мне {n} год')
elif 2 <= n % 10 <= 4:
    print(f'{n} года')



# 4.48. Определить, в какую из областей (I, II или III — рис. 4.8) 
# попадает точка с заданными координатами. 
# Для простоты принять, что точка не попадает на границы областей.

x = int(input('введите координату x '))
y = int(input('введите координату y '))

if x < 1:
    print('первая область')
elif 1 < x < 5:
    print('Вторая область')
elif x > 5:
    print('Третья область')

# ----------------------------------

alpha = 1
betta = 0

result = sin(alpha)*cos(betta) + cos(alpha)*sin(betta)
print(result)

# ----------------------------------------

num1 = randint(-10,10)
num2 = uniform(5, 10.5)
num3 = random()

print(num1,num2,num3)

# --------------------------------------

# range(start=0, end-1, step)
num = range(1,10) # 1,2,3,4,5,6,7,8,9
print(num)
# range(4) 0,1,2,3
# range(1,10,2) 1,3,5,7,9
# range(1,10+1)
# range(10,1,-1) 10,9,8,7,6,5,4,3,2
# range(0,10,2)

for number in range(10):
    print(20, end=' ')

# 6.3. Напечатать "столбиком": 
# а) все целые числа от 20 до 35; 
# б) квадраты всех целых чисел от 10 до b (значение b вводится с клавиатуры; b 10); 


for num in range(20,35+1):
    print(num)

b = 30
for num in range(10, b+1):
    print(num**2)

# 6.4. Напечатать числа следующим образом: 
# а) 10 10.4 
#     11 11.4
#         ... 
#     25 25.4 
# б) 25 25.5 24.8 
#     26 26.5 25.8 
#            ... 
#     35 35.5 34.8 

for num in range(10,25+1):
    print(num, num + 0.4, sep='  ')

for num in range(25, 35+1):
    print(num, num + 0.5, num - 0.2, sep='  ')

# 6.5. Напечатать числа следующим образом: 
# а) 21 19.2 
#     20 18.2 
#         ... 
#      10 8.2 
# б) 45 44.5 44.2 
#     44 43.5 43.2 
#             ... 
#      25 24.5 24.2 


for num in range(21, 10-1, -1):
    print(num, num - 1.8, sep='  ')

for num in range(45, 25-1, -1):
    print(num, num - 0.5, num - 0.8, sep='  ')

# 6.10. Напечатать таблицу умножения на 7: 
# 1 х 7 = 7 
# 2 х 7 = 14 
# ... 
# 9 х 7 = 63 

for num in range(1,10):
    print(f'{num} x {7} = {num*7}')

# 6.8. Напечатать таблицу соответствия между весом в фунтах и весом в килограммах для значений 1, 2, ..., 10 фунтов (1 фунт = 453 г). 

for i in range(1,10+1):
    print('Фунты Граммы')
    print(f'{i} = {i*453}')

# 6.15. Рассчитать значения z для значений a, равных 2, 3, ..., 17: 

for i in range(2,17+1):
    t  = 4 * i
    z = 3.5 * t**2 - 7 * t + 16
    print(int(z))
