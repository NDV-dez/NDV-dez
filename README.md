<h1 align="center">Hi there, I'm <a href="https://daniilshat.ru/" target="_blank">Dmitry</a> 
<img src="https://github.com/blackcater/blackcater/raw/main/images/Hi.gif" height="32"/></h1>
<h3 align="center">Computer science student</h3>
<h3 align="center"><img src="https://media4.giphy.com/media/v1.Y2lkPTZjMDliOTUyeXE3MDN1NXJzeXQ5c2lud2ZjZnlwZzlpeHl0NmNuN3FvNTMxcnhzaSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/VTtANKl0beDFQRLDTh/200w.gif"></h3>
https://docs.google.com/document/d/1mDpw0MKL5iw4DjmZhdo05GA9PZp0fbXatHB4lkcB0qE/edit?usp=drive_web&ouid=107694156041996626723
https://docs.google.com/document/d/1p3UIJq86shCDYvB5nrDFv_K1Fa0tUQq6bW1uDV3jndQ/edit?tab=t.0
# # 2.6. Дано двузначное число. Найти: 
# # а) число десятков в нем; 
# # б) число единиц в нем; 
# # в) сумму его цифр; 
# # г) произведение его цифр. 

# # 32
# # a)3 b)2 c)5 d)6

# number = int(input("Введите двузначное число: "))

# result_a = number // 10
# result_b = number % 10
# result_c = result_a + result_b
# result_d = result_a * result_b

# print(f'Пользователь ввел {number}.\nВ числе {number} хранится {result_a} десятков.\nВ числе {number} хранится {result_b} единиц')
# print(f'Сумма {result_a} + {result_b} = {result_c}\nПроизведение цифр {result_a} * {result_b} = {result_d}')
# # 2.7. Дано двузначное число. Получить число, образованное при перестановке цифр заданного числа.

# # 32 -> 23

# number_rev = int(input('Введите двузначное число: '))

# digit = number_rev // 10
# tens = number_rev % 10
# result = tens * 10 + digit
# # result = int(str(tens) + str(digit))
# print(result)

#digit = 2
#tens = 3
#32 -> 23
#digit * 10 + tens -> 2 * 10 + 3

# 2.8. Дано трехзначное число. Найти: 
# а) число единиц в нем;
# б) число десятков в нем; 
# в) сумму его цифр; 
# г) произведение его цифр. 

# number = int(input('Введите трехзначное число: '))

# digit = number % 10
# tens = number // 10 % 10
# hundreds = number // 100
# summ_num = digit + tens + hundreds
# mult_num = digit * tens * hundreds
# print(f'В числе {number} хранится {digit} единиц, {tens} десятков, {hundreds} сотен.')
# print(f'Произведение цифир числа {number} = {mult_num}\nСумма числа {number} = {summ_num}')

# 2.9. Дано трехзначное число. Найти число, полученное при прочтении его цифр справа налево. 

# number = int(input('Введите трехзначное число: '))

# digit = number % 10
# tens = number // 10 % 10
# hundreds = number // 100

# result = digit * 100 + tens * 10 + hundreds
# print(result)

# 2.10. Дано трехзначное число. В нем зачеркнули первую слева цифру и приписали ее в конце. Найти полученное число. 

# number = int(input('Введите трехзначное число: '))

# last_num = number // 100
# result = number % 100 * 10 + last_num
# print(result)

# Дано трехзначное число. В нем зачеркнули последнюю справа цифру и приписали ее в начале. Найти полученное число. 


# number = int(input('Введите трехзначное число: '))

# last_num = number % 10
# result = last_num * 100 + number // 10
# print(result)

# 2.12. Дано трехзначное число. Найти число, полученное при перестановке первой и второй цифр заданного числа. 

# number = int(input('Введите трехзначное число: '))

# digit = number % 10
# tens = number // 10 % 10
# hundreds = number // 100
# result = tens * 100 + hundreds * 10 + digit
# print(result)

# 123 - > 213  2*100=200 1*10=10 3

# 2.13. Дано трехзначное число. Найти число, полученное при перестановке второй и третьей цифр заданного числа. 

# number = int(input('Введите трехзначное число: '))

# digit = number % 10
# tens = number // 10 % 10
# hundreds = number // 100
# result = hundreds*100 + digit*10 +tens
# print(result)
# #123 132 100 + 30 + 2

# 2.14. Дано трехзначное число, в котором все цифры различны. Получить шесть чисел, образованных при перестановке цифр заданного числа.

number = int(input('Введите трехзначное число: '))

digit = number % 10
tens = number // 10 % 10
hundreds = number // 100
result_1 = hundreds*100 + digit*10 +tens
result_2 = hundreds*10 + digit*100 +tens
result_3 = hundreds + digit*10 +tens*100
result_4 = hundreds + digit*100 +tens*10
result_5 = hundreds*10 + digit +tens*100
result_6 = hundreds*100 + digit +tens*10
print(result_1,result_2,result_3,result_4,result_5,result_6)
