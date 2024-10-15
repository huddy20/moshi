
# Тема 6. Базовые коллекции: словари, кортежи 
Отчет по Теме #6 выполнил(а):
- Топорищев Никита Олегович
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### В школе, где вы учились, узнали, что вы крутой программист и попросили написать программу для учителей, которая будет при вводе кабинета писать для него ключ доступа и статус, занят кабинет или нет. 
request = int(input('Введите номер кабинета: '))

dictionary = {

101: {'key': 1234, 'access': True},

102: {'key': 1337, 'access': True},

103: {'key': 8943, 'access': True},

104: {'key': 5555, 'access': False},

None: {'key': None, 'access': False},

}

response = dictionary.get(request)

if not response:

response = dictionary[None]

key = response.get('key')

access = response. get('access')

print(key, access)

### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen1.jpg)

## Выводы
Код запрашивает у пользователя номер кабинета и проверяет, есть ли такой кабинет в словаре. Если номер существует, то программа выводит ключ и значение параметра access для этого кабинета.

## Лабораторная работа №2
### Алексей решил создать самый большой словарь в мире. Для этого он придумал функцию dict_maker (**kwargs), которая принимает неограниченное количество параметров «ключ: значение» и обновляет созданный им словарь my_dict, состоящий всего из одного элемента «first» со значением «so easy». Помогите Алексею создать данную функцию.
from pprint import pprint

my_dict = {'first': 'so easy'}

def dict_maker(**kwargs) :

my_dict.update(**kwargs)

dict_maker(a1=1, a2=20, a3=54, a4=13)

dict_maker(name='Михаил', age=31, weight=70, eyes_color='blue')

pprint(my_dict)
### Результат
  ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen2.jpg)

## Выводы
Код создаёт словарь с помощью функции dict_maker(), которая принимает произвольное количество именованных аргументов (**kwargs) и добавляет их в существующий словарь my_dict с помощью метода .update().

## Лабораторная работа №3
### Для решения некоторых задач бывает необходимо разложить строку на отдельные символы. Мы знаем что это можно сделать при помощи split(), у которого более гибкая настройка для разделения для этого, но если нам нужно посимвольно разделить строку без всяких условий, то для этого мы можем использовать кортежи (tuple). 
input_string = 'HelloWorld'

result = tuple(input_string)

print(result)

print (list (result))

### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen3.jpg)

## Выводы
Код принимает строку 'HelloWorld' и преобразует её в кортеж с помощью функции tuple(), а затем выводит полученный кортеж, после снова печатает преобразованный кортеж, но уже как список с помощью функции list(), которая преобразует кортеж в список.
  
## Лабораторная работа №4
### Вовочка решил написать крутую функцию, которая будет писать имя, возраст и место работы, но при этом на вход этой функции будет поступать кортеж. Помогите Вовочке написать эту программу.
def personal_info(name, age, company='unnamed' ):

print(f"Имя: {name} Возраст: {age} Компания: {company}")

tom = ("Григорий", 22)

personal_info(*tom)

bob = ("Георгий", 41, "Yandex")

personal_info(*bob)

### Результат

 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen4.jpg)
## Выводы
Функция выводит на экран строку с информацией о человеке, используя переданные аргументы.

## Лабораторная работа №5
### Для сопровождения первых лиц государства X нужен кортеж, но никто не может определиться с порядком машин, поэтому вам нужно написать функцию, которая будет сортировать кортеж, состоящий из целых чисел по возрастанию, и возвращает его. Если хотя бы один элемент не является целым числом, то функция возвращает исходный кортеж.
def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen5.jpg)

## Выводы
Сортировка и возвращение кортежа

## Самостоятельная работа №1
### При создании сайта у вас возникла потребность обрабатывать данные пользователя в странной форме, а потом переводить их в нужные вам форматы. Вы хотите принимать от пользователя последовательность чисел, разделенных пробелом, а после переформатировать эти данные в список и кортеж. Реализуйте вашу задумку. Для получения начальных данных используйте input(). Результатом программы будет выведенный список и кортеж из начальных данных.

'#' Get user input as a space-separated string of numbers

user_input = input("Введите последовательность чисел, разделенных пробелом: ")

'#' Split the input string by spaces to form a list

numbers_list = user_input.split()

'#' Convert the list into a tuple

numbers_tuple = tuple(numbers_list)

'#' Output the list and tuple

print("Список:", numbers_list)

print("Кортеж:", numbers_tuple)

### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen6.jpg)

## Выводы 
Код запрашивает у пользователя ввод последовательности чисел, разделённых пробелами, разбивает строку на список, преобразует его в кортеж и выводит оба результата на экран.
## Самостоятельная работа №2
### Николай знает, что кортежи являются неизменяемыми, но он очень упрямый и всегда хочет доказать, что он прав. Студент решил создать функцию, которая будет удалять первое появление определенного элемента из кортежа по значению и возвращать кортеж без него. Попробуйте повторить шедевр не признающего авторитеты начинающего программиста.  

def remove_first_occurrence(tpl, value):
   
if value in tpl:
        
temp_list = list(tpl)
       
temp_list.remove(value)
       
return tuple(temp_list)
        
else:
       
return tpl

test_1 = remove_first_occurrence((1, 2, 3), 1)
test_2 = remove_first_occurrence((1, 2, 3, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2), 3)
test_3 = remove_first_occurrence((2, 4, 6, 6, 4, 2), 9)

print(test_1)  # Ожидаемый результат: (2, 3)
print(test_2)  # Ожидаемый результат: (1, 2, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2)
print(test_3)  # Ожидаемый результат: (2, 4, 6, 6, 4, 2)

### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen7.jpg)

## Вывод
Этот код определяет функцию remove_first_occurrence, которая удаляет первое вхождение указанного значения из кортежа. Если значение присутствует, кортеж преобразуется в список, из которого удаляется первое вхождение элемента, а затем список возвращается в виде кортежа. Если элемента нет, возвращается исходный кортеж.
 
## Самостоятельная работа №3
### Ребята поспорили кто из них одним нажатием на numpad наберет больше повторяющихся цифр, но не понимают, как узнать победителя. Вам им нужно в этом помочь. Дана строка в виде случайной последовательности чисел от 0 до 9 (длина строки минимум 15 символов). Требуется создать словарь, который в качестве ключей будет принимать данные числа (т. е. ключи будут типом int), а в качестве значений – количество этих чисел в имеющейся последовательности. Для построения словаря создайте функцию, принимающую строку из цифр. Функция должна возвратить словарь из 3-х самых часто встречаемых чисел, также эти значения нужно вывести в порядке возрастания ключа.

from collections import Counter

def find_top_three_frequent_numbers(number_string):
    
number_counts = Counter(map(int, number_string))
 
top_three = number_counts.most_common(3)
    
top_three_dict = {k: v for k, v in sorted(top_three)}

return top_three_dict

number_string = "12345678901234567890123456789012345" 

result = find_top_three_frequent_numbers(number_string)

print(result)  # Словарь из 3 самых часто встречающихся чисел

### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen8.jpg)

## Вывод
Этот код определяет функцию find_top_three_frequent_numbers, которая принимает строку, содержащую числа, и находит три самых частых числа в этой строке. В результате функция возвращает словарь, содержащий три самых часто встречающихся числа и их количества. В примере использования, строка "12345678901234567890123456789012345" передаётся в функцию, и выводится словарь с результатами.

## Самостоятельная работа №4
### Ваш хороший друг владеет офисом со входом по электронным картам, ему нужно чтобы вы написали программу, которая показывала в каком порядке сотрудники входили и выходили из офиса. Определение сотрудника происходит по id. Напишите функцию, которая на вход принимает кортеж и случайный элемент (id), его можно придумать самостоятельно. Требуется вернуть новый кортеж, начинающийся с первого появления элемента в нем и заканчивающийся вторым его появлением включительно. Если элемента нет вовсе – вернуть пустой кортеж. Если элемент встречается только один раз, то вернуть кортеж, который начинается с него и идет до конца исходного.
    def process_entry_exit(tpl, employee_id):
    # Проверяем, есть ли элемент в кортеже
    if employee_id not in tpl:
        return ()  # Возвращаем пустой кортеж, если элемента нет вовсе

    # Находим индекс первого появления
    first_index = tpl.index(employee_id)

    # Проверяем, встречается ли элемент еще раз
    if tpl.count(employee_id) > 1:
        # Находим индекс второго появления
        second_index = tpl.index(employee_id, first_index + 1)
        return tpl[first_index:second_index + 1]
    else:
        # Если элемент только один раз, возвращаем кортеж с начала первого появления до конца
        return tpl[first_index:]

    # Примеры использования функции
    test_1 = process_entry_exit((1, 2, 3), 8)
    test_2 = process_entry_exit((1, 8, 3, 4, 8, 8, 9, 2), 8)
    test_3 = process_entry_exit((1, 2, 8, 5, 1, 2, 9), 8)

    # Вывод результатов
    print(test_1)  # Ожидаемый результат: ()
    print(test_2)  # Ожидаемый результат: (8, 3, 4, 8)
    print(test_3)  # Ожидаемый результат: (8, 5, 1, 2, 9)


### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen9.jpg)

## Вывод
Этот код определяет функцию process_entry_exit, которая обрабатывает кортеж сотрудников по их идентификатору employee_id, функция позволяет извлекать последовательности идентификаторов сотрудников, начиная с первого появления указанного идентификатора и заканчивая его вторым появлением (если оно есть), или просто возвращает всё с первого появления до конца.

## Самостоятельная работа №5
### Самостоятельно придумайте и решите задачу, в которой будут обязательно использоваться кортеж или список. Проведите минимум три теста для проверки работоспособности вашей задачи. Задача: Упорядочивание оценок студентов. Напишем функцию, которая принимает список оценок студентов и возвращает кортеж, содержащий уникальные оценки в порядке возрастания, а также их количество.

    def process_grades(grades):
    # Преобразуем список в множество, чтобы получить уникальные оценки
    unique_grades = set(grades)
    
    # Преобразуем множество в отсортированный список
    sorted_grades = sorted(unique_grades)
    
    # Подсчитываем количество уникальных оценок
    count = len(sorted_grades)
    
    # Возвращаем кортеж: (количество уникальных оценок, список уникальных оценок)
    return count, tuple(sorted_grades)

    # Тесты
    def run_tests():
    # Тест 1
        grades_1 = [5, 3, 4, 3, 2, 5, 1, 4]
        result_1 = process_grades(grades_1)
        print(f"Тест 1: {result_1} (Ожидаемый результат: (5, (1, 2, 3, 4, 5)))")

    # Тест 2
        grades_2 = [3, 3, 3, 3, 3]
        result_2 = process_grades(grades_2)
        print(f"Тест 2: {result_2} (Ожидаемый результат: (1, (3,)))")

    # Тест 3
        grades_3 = [2, 4, 6, 2, 5, 5, 6, 7]
        result_3 = process_grades(grades_3)
        print(f"Тест 3: {result_3} (Ожидаемый результат: (6, (2, 4, 5, 6, 7)))")

    # Запуск тестов
    run_tests()


### Результат
 ![Меню](https://github.com/huddy20/moshi/raw/main/image/l6_screen10.jpg)

## Вывод
Функция process_grades принимает список оцено, преобразует его в множество, чтобы получить уникальные значения. Сортирует уникальные оценки и подсчитывает их количество, авзвращает кортеж, содержащий количество уникальных оценок и отсортированный кортеж уникальных оценок. Запустив run_tests(), мы получим результаты тестов, позволяя убедиться в корректности работы функции.
## Общие выводы по теме
Базовые коллекции в Python, такие как словари и кортежи, играют важную роль в организации и управлении данными. Словари представляют собой неупорядоченные коллекции пар "ключ-значение", что позволяет эффективно хранить и извлекать данные по уникальным ключам. Они удобны для быстрого доступа к информации и идеально подходят для ситуаций, где необходимо ассоциировать данные. Кортежи, в свою очередь, являются неизменяемыми последовательностями, что делает их полезными для хранения фиксированных наборов данных. Их неизменяемость обеспечивает безопасность данных и позволяет использовать их в качестве ключей в словарях или элементов множеств.
