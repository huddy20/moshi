# Тема 3. Операторы, условия, циклы
Отчет по Теме #3 выполнил(а):
- Топорищев Никита Олегович
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + |
| Задание 7 | + |
| Задание 8 | + |
| Задание 9 | + |
| Задание 10 | + |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Создайте две переменные, значение которых будете вводить через консоль. Также составьте условие, в котором созданные ранее переменные будут сравниваться, если условие выполняется, то выведете в консоль «Выполняется», если нет, то «Не выполняется».

one = int(input("Введите значение первой переменной: "))

two = int(input("Введите значение второй переменной: "))

if one >= two:

print("Выполняется")
    
else:

print("Не выполняется")
    
### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen1.jpg)

## Выводы

Реализован ввод двух переменных и вывод соответствующего сообщения при проверке на условие

## Лабораторная работа №2
### Напишите программу, которая будет определять значения переменной меньше 0, больше 0 и меньше 10 или больше 10. Это нужно реализовать при помощи одной переменной, значение которой будет вводится через консоль, а также при помощи конструкций if, elif, else.

one = int(input("Введите значение переменной: "))

if one < 0:

    print("Переменная меньше 0")
    
elif 0 < one < 10:

    print("Переменная больше 0 и меньше 10")
    
else:

    print("Переменная больше 10")

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen2.jpg)


## Выводы

Условиями, с помощью if, elif, else проверяем в каком диапозоне число

## Лабораторная работа №3
### Напишите программу, в которой будет проверяться есть ли переменная в указанном массиве используя логический оператор in. Самостоятельно посмотрите, как работает программа со значениями которых нет в массиве numbers.

numbers = [1, 3, 4, 6, 8, 9]

value = int(input("Введите значение переменной "))

if value in numbers:

    print("Переменная есть в этом массиве")
    
else:

    print("Переменной нет в этом массиве")
    
### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen3.jpg)


## Выводы

Проверяем есть ли введенное число в массиве с помощью if value in

## Лабораторная работа №4
### Напишите программу, которая будет определять находится ли переменная в указанном массиве и если да, то проверьте четная она или нет. Самостоятельно протестируйте данную программу с разными значениями переменной value.

numbers = [1, 3, 4, 6, 8, 9, 15, 16, 73, 321, 322]

value = int(input("Введите значение переменной "))

if value in numbers:

    if value % 2 == 0:
    
        print("Переменная четная и есть в этом массиве")
        
    else:
    
        print("Переменная нечетная и есть в этом массиве")
        
else:

    print(f"Переменной нет в массиве и она равна {value}")
    
### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen4.jpg)


## Выводы

Определяем четная переменная или нет и есть ли она в массиве

## Лабораторная работа №5
### Напишите программу, в которой циклом for значения переменной i будут меняться от 0 до 10 и посмотрите, как разные виды сравнений и операций работают в цикле.

for i in range(10):

    print('i = ', i)
    
    if i == 0:
    
        i += 2
        
    if i == 1:
    
        continue
        
    if i == 2 or i == 3:
    
        print('Переменная равна 2 или 3')
        
    elif i in [4, 5, 6]:
    
        print('Переменная равна 4, 5 или 6')
        
    else:
    
        break

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen5.jpg)


## Выводы

Разные виды сравнений и операций

## Лабораторная работа №6
### Напишите программу, в которой при помощи цикла for определяется есть ли переменная value в строке string и посмотрите, как работает оператор else для циклов. Самостоятельно посмотрите, что выведет программа, если значение переменной value оказалось в строке string.

string = 'Привет всем изучающим Python!'

value = input()

for i in string:

    if i == value:
    
        index = string.find(value)
        
        print(f"Буква '{value}' есть в строке под {index} индексом")
        
        break
        
else:

    print(f"Буквы '{value}' нет в указанной строке")
    
### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen6.jpg)


## Выводы

Проверка на наличие буквы в строке

## Лабораторная работа №7
### Напишите программу, в которой вы наглядно посмотрите, как работает цикл for проходя в обратном порядке, то есть, к примеру не от 0 до 10, а от 10 до 0. В уже готовой программе показано вычитание из 100, а вам во время реализации программы будет необходимо придумать свой вариант применения обратного цикла.

value = 100

for i in range(10, -1, -1):

    value -= i
    
    print(i, value)

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen7.jpg)


## Выводы

Наглядная работа цикла for

## Лабораторная работа №8
### Напишите программу используя цикл while, внутри которого есть какие-либо проверки, но быть осторожным, поскольку циклы while при неправильно написанных условиях могут становиться бесконечными.

value = 0

while value < 20:

    if value == 0:
    
        value += 1
        
    elif value // 5 > 1:

        value += 2
        
    else:
    
        value += 5
        
    print(value)

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen8.jpg)


## Выводы

Проверки в цикле while

## Лабораторная работа №9
### Напишите программу с использованием вложенных циклов и одной проверкой внутри них. Самое главное, не забудьте, что нельзя использовать одинаковые имена итерируемых переменных, когда вы используете вложенные циклы.

value = 0

for i in range(10):

    for j in range(10):
    
        if i != j:
        
            value += j
            
        else:
        
            pass
            
print(value)

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen9.jpg)


## Выводы

Вложенные циклы с условием внутри

## Лабораторная работа №10
### Напишите программу с использованием flag, которое будет определять есть ли нечетное число в массиве. В данной задаче flag выступает в роли индикатора встречи нечетного числа в исходном массиве, четных чисел.

even_array = [2, 4, 6, 8, 9]

flag = False

for value in even_array:

    if value % 2 == 1:
    
        flag = True
        


if flag is True:

    print('В массиве есть нечетное число')
    
else:

    print('В массиве все числа четные')
    
### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen10.jpg)


## Выводы

Проверка на наличие нечетного числа в массиве при помощи переменной flag (bool)

## Самостоятельная работа №1
### 1)	Напишите программу, которая преобразует 1 в 31. Для выполнения поставленной задачи необходимо обязательно и только один раз использовать: цикл for; *=5; +=1. Никаких других действий или циклов использовать нельзя.

result = 1

result *= 5

for i in range(26):

    result += 1
    

print(result)

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen11.jpg)

## Выводы

Восстановление файла к предыдущему состоянию

## Самостоятельная работа №2
### Напишите программу, которая фразу «Hello World» выводит в обратном порядке, и каждая буква находится в одной строке консоли. 

for char in reversed("Hello World"):

    print(char)

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen12.jpg)

## Выводы

Программа использует функцию reversed() для переворота строки и выводит каждый символ строки на новой строке с помощью цикла for. Таким образом, фраза "Hello World" выводится в обратном порядке с переносом каждой буквы на новую строку.

## Самостоятельная работа №3
### Исправление коммита

num = input("Введите число: ")


if not num.isdigit() or not (0 <= int(num) <= 10):

    print("Ошибка: число должно быть от 0 до 10 включительно.")
    
else:

    num = int(num)

    if 0 <= num <= 3:
    
        print("от 0 до 3 включительно")
        
    elif 3 < num <= 6:
    
        print("от 3 до 6")
        
    else:
    
        print("от 6 до 10 включительно")

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen13.jpg)
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen14.jpg)

## Выводы

Программа проверяет, введено ли корректное число в диапазоне от 0 до 10. Если число находится в указанном диапазоне, программа определяет, в какой из трёх диапазонов оно попадает (0-3, 3-6, 6-10) и выводит соответствующее сообщение. Если введено некорректное значение, программа уведомляет об этом и завершает работу.

## Самостоятельная работа №4
### Манипулирование строками. Напишите программу на Python, которая принимает предложение (на английском) в качестве входных данных от пользователя. Выполните следующие операции и отобразите результаты:

sentence = input("Введите предложение на английском: ")

length = len(sentence)

print(f"Длина предложения: {length}")

lower_sentence = sentence.lower()

print(f"Предложение в нижнем регистре: {lower_sentence}")

vowels = 'aeiou'

vowel_count = sum(1 for char in lower_sentence if char in vowels)

print(f"Количество гласных: {vowel_count}")

replaced_sentence = lower_sentence.replace("ugly", "beauty")

print(f"Замена 'ugly' на 'beauty': {replaced_sentence}")

starts_with_the = sentence.startswith("The")

ends_with_end = sentence.endswith("end")

print(f"Начинается с 'The': {starts_with_the}")

print(f"Заканчивается на 'end': {ends_with_end}")


### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen15.jpg)
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen16.jpg)
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen17.jpg)

## Выводы

Эта программа демонстрирует основные операции по манипулированию строками в Python:

Подсчёт длины предложения показывает, сколько символов содержится в строке, включая пробелы и знаки препинания.

Перевод строки в нижний регистр полезен, если нужно провести нечувствительные к регистру сравнения или обработку текста. Например, это используется для подсчёта гласных.

Подсчёт количества гласных даёт количество букв a, e, i, o, u, которые встречаются в предложении. Программа использует цикл, чтобы пройти по каждому символу строки и проверить, является ли он гласной.

Замена слов позволяет заменить все вхождения слова "ugly" на "beauty". Это демонстрирует работу с заменой подстрок в Python с помощью метода replace().

Проверка начала и конца строки с использованием методов startswith() и endswith() — простой способ узнать, соответствует ли строка определённому шаблону.

## Самостоятельная работа №5
### Настройка .gitignore

### Результат.
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l3_screen18.jpg)

## Выводы

gitignore
