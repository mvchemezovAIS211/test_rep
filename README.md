# Тема 4. Функции и модули
Отчет по Теме #4 выполнил:
- Чемезов Михаил Владимирович
- АИС-21-1

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
- Напишите функцию, которая выполняет любые арифметические 
действия и выводит результат в консоль. Вызовите функцию используя “точку входа”.
### Код
```python
def main():
    print(3+5)


if __name__ == '__main__':
    main()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab1.png)
### Вывод:
- Пользователь вводит два значения, которые сохраняются в переменные one и two соответственно.
- Затем выполняется условие if one >= two, которое сравнивает значения переменных one и two. Если one больше или равно two, то условие считается истинным.
- Если условие истинно, то выводится сообщение 'Выполняется'.
- Если условие ложно, то выводится сообщение 'Не выполняется'.

## Лабораторная работа №2
- Напишите функцию, которая выполняет любые арифметические 
действия, возвращает при помощи return значение в место, откуда 
вызывали функцию. Выведите результат в консоль. Вызовите функцию используя “точку входа”.
### Код
```python
def main():
    result = 3+9
    return result


if __name__ == '__main__':
    answer = main()
    print(answer)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab2.png)
### Вывод:
- Строка one = int(input('Введите значение переменной: ')) предлагает пользователю ввести значение переменной и сохраняет его в переменной one, преобразуя в целое число с помощью функции int().
- Строка if one < 0: проверяет условие: если значение переменной one меньше нуля, выполняется код внутри блока if. В данном случае, если переменная меньше 0, выводится сообщение "Переменная меньше 0".
- Строка elif 0 < one < 10: проверяет второе условие: если значение переменной one больше нуля и меньше 10, выполняется код внутри блока elif. Если это условие истинно, выводится сообщение "Переменная больше 0 и меньше 10".
- Если ни одно из предыдущих условий не выполняется, то выполняется код в блоке else. В данном случае, выводится сообщение "Переменная больше 10".

## Лабораторная работа №3
- Напишите функцию, в которую передаются два аргумента, над ними производится арифметическое действие, результат возвращается туда, откуда эту функцию вызывали. Выведите результат в консоль. 
Вызовите функцию в любом небольшом цикле.
На скриншоте ниже приведен пример программы, в которой аргумент функции  “x“превращается в параметр “one”, то же самое происходит с “y” и “two”
### Код
```python
def main(one, two):
    result = one + two
    return result


for i in range(5):
    answer = main(one=1, two=8)
    print(answer)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab3.png)
### Выводы:
- Создается список numbers с некоторыми числами.
- Пользователю предлагается ввести значение переменной с помощью вызова input(), и это значение преобразуется в целое число с помощью int().
- Затем код проверяет, находится ли введенное значение в списке numbers с помощью оператора in.
- Если значение присутствует в списке, выводится сообщение "Переменная есть в данном массиве".
- В противном случае выводится сообщение "Переменной нет в этом массиве".
  
## Лабораторная работа №4
- Напишите функцию, на вход которой подается какое-то изначальное 
неизвестное количество аргументов, над которыми будет производится арифметические действия. Для выполнения задания необходимо 
использовать кортеж “*args”. На скриншоте ниже приведен пример 
такой программы с комментариями. 
Для закрепления понимания работы с кортежами настоятельно 
рекомендуем поменять аргументы вызова функции, вручную посчитать результат, только потом запустить программу с новыми значениями и проверить себя, насколько вы поняли данный аспект 
программирования.
### Код
```python
def main(x, *args):
    one = x #10
    two = sum(args) # 4, 2, 2, -1, 0, -1, -2, 2
    three = float(len(args)) #длина кортежа args
    # пример работы операций над параметрами функции
    print(f"one={one}\ntwo={two}\nthree={three}")

    return x + sum(args) / float(len(args))


if __name__ == '__main__':
    result = main(10, 4, 2, 2, -1, 0, -1, -2, 2)
    print(f"\nresult={result}")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab4.png)
### Выводы:
- Данный код анализирует введенное пользователем значение переменной и проверяет его наличие в списке numbers. Если значение присутствует в списке, то дальше происходит проверка на четность.
- Если значение является четным (делится на 2 без остатка), то выводится сообщение "Переменная чётная и есть в данном массиве". В противном случае, если значение нечетное, выводится сообщение "Переменная нечётная и есть в данном массиве".
- Если введенное значение переменной не присутствует в списке numbers, то выводится сообщение "Переменная нет в массиве numbers и она равна Value ", где Value заменяется на фактическое значение переменной, введенное пользователем.

## Лабораторная работа №5
- Напишите функцию, которая на вход получает кортеж “**kwargs” и при помощи цикла выводит значения, поступившие в функцию. На скриншоте ниже указаны два варианта вызова функции с “**kwargs” и два варианта работы с данными, поступившими в эту функцию. 
Комментарии в коде и теоретическая часть помогут вам разобраться в этом нелегком аспекте. Вызовите функцию используя “точку входа”.
### Код
```python
def main(**kwargs):
    for i in kwargs.items():
        print(i[0], i[1])

    print()

    for key in kwargs:
        print(f"{key} = {kwargs[key]}")


if __name__ == '__main__':
    main(x=[1, 2, 3], y=[3,3,0], z=[2,3,0], w=[3,3,0], h=[3,3,0])
    print()
    main(**{'x': [1,2,3], 'y': [3,3,0]})
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab5.png)
### Выводы:
- Сначала код печатает текущее значение i.
- Если i равно 0, к значению i добавляется 2. Однако, эта операция не влияет на весь цикл, так как в Python цикл for не видит изменения счетчика внутри цикла. Это означает, что даже если вы измените значение i внутри цикла, в следующей итерации i все равно будет увеличено на 1 от предыдущего исходного значение, а не от измененного значения.
- Если i равно 1, то с помощью команды continue цикл пропускает все остальное и переходит к следующей итерации.
- Если i равно 2 или 3, код печатает "Переменная равна 2 или 3". Здесь есть синтаксическая ошибка: тройное равенство === не существует в Python, и это должно быть изменено на ==.
- Если i равняется одному из чисел в списке [4, 5, 6], код печатает "Переменная равна 4, 5 или 6".
- Во всех остальных случаях код выходит из цикла с помощью break.

## Лабораторная работа №6
- Напишите две функции. Первая – получает в виде параметра 
“**kwargs”. Вторая считает среднее арифметическое из значений 
первой функции. Вызовите первую функцию используя “точку входа” и минимум 4 аргумента.
### Код
```Python
def main(**kwargs):
    for i, j in kwargs.items():
        print(f"{i}. Mean = {mean(j)}")

    print()

def mean(data):
    return sum(data) / float(len(data))


if __name__ == '__main__':
    main(x=[1, 2, 3], y=[3,3,0])
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab6.png)
### Вывод:
- Этот код Python принимает входные данные от пользователя в форме одного символа (например, буквы), и затем ищет этот символ в заданной строке (в данном случае, строка это "Привет всем изучающим Python!").
- После того как пользователь вводит значение, код начинает перебирать каждый символ в строке. Если символ, введенный пользователем, совпадает с одним из символов в строке, код находит и выводит индекс этого символа. Индекс - это позиция символа в строке (отсчет начинается с нуля). Поиск прекращается после первого совпадения.
- Если же символа, введенного пользователем, нет в строке, выводится сообщение о его отсутствии.
- Стоит учитывать что код обрабатывает строчные и заглавные букву как разные символы.

## Лабораторная работа №7
- Создайте дополнительный файл .py. Напишите в нем любую функцию, которая будет что угодно выводить в консоль, но не вызывайте ее в нем. Откройте файл main.py, импортируйте в него функцию из нового файла и при помощи “точки входа” вызовите эту функцию.
### Код
- Код в файле for_import.py
```Python
def say_hello():
    print('Hello students!')
```
- Основной код
```Python
from for_import import say_hello

if __name__ == '__main__':
    say_hello()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab7.png)
### Выводы:
- Задает начальное значение переменной value равное 100.
- Выполняет цикл, который итерируется по диапазону начиная с 10 и идет в обратном порядке до 0 (включая его) с шагом -1. Это значит, что переменная цикла i принимает значения от 10 до 0 последовательно в обратном порядке.
- В теле цикла от переменной value вычитается 1 (value -= 1).
- Затем, при каждой итерации цикла на экран выводятся два значения - значение i и value - в формате (i, value).

## Лабораторная работа №8
- Напишите программу, которая будет выводить корень, синус, косинус полученного от пользователя числа.
### Код
```Python
from math import sqrt, sin, cos


def main():
    value = int(input('Введите значение: '))
    print(sqrt(value))
    print(sin(value))
    print(cos(value))


if __name__ == '__main__':
    main()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab8.png)
### Выводы:
- value = 0 вводит переменную value и задает ей начальное значение 0.
- while value < 100: устанавливает цикл, который будет выполняться до тех пор, пока value остается меньше 100.
- В цикле есть условное выражение if-elif-else:
- Если value равно 0, чтобы не возникло бесконечного цикла, value увеличивается на 10.
- Если value // 5 превышает 1 (целочисленное деление value на 5), то value умножается на 5.
- Во всех остальных случаях value уменьшается на 5.
- print(value) выводит текущее значение value на каждой итерации цикла.
- код произведет следующую последовательность действий:
     - 1) Изначально value равно 0, поэтому будет выполняться первая ветка условия, и к value прибавляется 10. Печатается число 10.
     - 2) Далее value равно 10, но 10 // 5 равно 2, что больше 1. Значит, выполнится вторая ветка условия: value умножится на 5. Печатается число 50.
     - 3) Теперь value равно 50, 50 // 5 равно 10, что больше 1, поэтому снова выполнится вторая ветка условия: value умножится на 5. Печатается число 250.
     - 4) Теперь value равно 250. 'While value  < 100' становится ложным и цикл завершается.

## Лабораторная работа №9
- Напишите программу, которая будет рассчитывать какой день недели будет через n-нное количество дней, которые укажет пользователь.
### Код
```Python
from datetime import datetime as dt
from datetime import timedelta as td



def main():
    print(
        f"Сегодня {dt.today().date()}. "
        f"День недели - {dt.today().isoweekday()}"
    )
    n = int(input('Введите количество дней: '))
    today = dt.today()
    result = today + td(days=n)
    print(
        f"Через {n} дней будет {result.date()}. "
        f"День недели - {result.isoweekday()}"
    )


if __name__ == '__main__':
    main()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab9.png)
### Выводы:
- Данный код на языке Python выполняет двойной цикл, где каждый цикл итерируется через диапазон чисел от 0 до 9 (10 чисел всего).
- Вложенные циклы перебирают все возможные пары (i, j), где i и j изменяются от 0 до 9. Если i не равно j, то j добавляется к переменной value. Если i равно j (что равносильно паре чисел вида (0,0), (1,1), (2,2), и так далее до (9,9)), то цикл продолжает свое выполнение, не увеличивая value.
- Таким образом, сумма будет происходить по каждому диапазону от 0 до 9, исключая само число диапазона. Например, для i=0, j будет перебирать значения от 1 до 9, а для i=1, j переберет значения: 0, 2, 3, 4, 5, 6, 7, 8, 9, и так далее.
- Итоговое значение value будет равно сумме всех чисел от 0 до 9 умноженных на 9 (так как каждое число суммируется 9 раз, исключая свое собственное значение). Это даст value = 9 * (0 + 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9) = 9 * 45 = 405.
- 'pass' просто проигнорируется, когда i равны j.

## Лабораторная работа №10
- Напишите программу с использованием глобальных переменных, которая будет считать площадь треугольника или прямоугольника в 
зависимости от того, что выберет пользователь. Получение всей 
необходимой информации реализовать через input(), а подсчет 
площадей выполнить при помощи функций. Результатом программы будет число, равное площади, необходимой фигуры.
### Код
```Python
global result


def rectangle():
    a = float(input("Ширина: "))
    b = float(input("Высота: "))
    global result
    result = a * b


def triangle():
    a = float(input("Основание: "))
    h = float(input("Высота: "))
    global result
    result = 0.5 * a * h


figure = input("1-прямоугольник, 2-треугольник: ")

if figure == '1':
    rectangle()
elif figure == '2':
    triangle()

print(f"Площадь: {result}")
```
### Результат
- площадь прямоугольника:
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab10_1.png)
- площадь треугольника:
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_4/pic/Lab10_2.png)
### Выводы:
- определена переменная even_array, которая представляет из себя список чисел: 2, 4, 6, 8 и 9.
- flag объявлена как False. Этот флаг будет использоваться для отслеживания, есть ли в массиве нечетное число.
- Следующий блок кода - это цикл for, который проходит через каждый элемент в even_array.
- Внутри цикла for происходит проверка, является ли число нечетным. Это достигается путем использования оператора модуля (% 2), который возвращает остаток от деления на 2. Если число нечетное, остаток будет 1 (в данном случае value % 2 == 1 вернет True), и flag устанавливается в True.
- После того, как цикл выполнен, производится окончательная проверка: если flag равен True (или же, сказано другим способом, если он True), то печатается сообщение 'В массиве есть нечётное число'. В противном случае, когда flag все еще False, печатается сообщение 'В массиве все числа чётные'.
- В данном вводе even_array содержит одно нечетное число (9), поэтому, после выполнения кода, выводом будет 'В массиве есть нечётное число'.

## Самостоятельная работа №1
- Дайте подробный комментарий для кода, написанного ниже. 
Комментарий нужен для каждой строчки кода, нужно описать что она делает. Не забудьте, что функции комментируются по-особенному.
![image](https://github.com/mvchemezov1/software-engineering/assets/144443468/73816df5-d9c7-4194-b927-6dcbdc4baad1)
### Код
```python
num = 1
for _ in range(2):
    num *= 5
    num += 1
print(num)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I1.png)
### Выводы:
- 'num = 1' создается переменная с именем num и присваивается ей значение 1.
- Затем выполняется цикл for два раза (for _ in range(2):). Прочерк (_) часто используется в Python, когда итерационная переменная цикла for не используется внутри самого цикла.
- Внутри цикла, в строке num *= 5, значение num умножается на 5, а затем новое значение присваивается num (num = num * 5).
- Затем, на следующей строке num += 1, выполнится операция инкремента: к num добавляется 1 (num = num + 1).
- После завершения цикла, последней строкой (print(num)) выводится результат - текущее значение переменной num.
- Выполнение кода:
-- num = 1
-- Первая итерация цикла (num * 5 + 1 = 6)
-- Вторая итерация цикла (num * 5 + 1 = 31)
-- Будет число 31.

## Самостоятельная работа №2
- Напишите программу, которая будет заменять игральную кость с 6 
гранями. Если значение равно 5 или 6, то в консоль выводится «Вы победили», если значения 3 или 4, то вы рекурсивно должны вызвать эту же функцию, если значение 1 или 2, то в консоль выводится «Вы проиграли». При этом каждый вызов функции необходимо выводить в консоль значение “кубика”. Для выполнения задания необходимо использовать стандартную библиотеку random. Программу нужно написать, используя одну функцию и “точку входа”
### Код
```python
message = "Hello World"
for i in range(len(message)-1, -1, -1):
        print(message[i])
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I2.png)
### Выводы:
- 'message = "Hello World"' Здесь объявляется переменная message, которая содержит строку "Hello World".
- 'for i in range(len(message)-1, -1, -1):' : Здесь устанавливается цикл for. Указанная функция range() создает последовательность чисел от len(message)-1 до 0. len(message)-1 является индексом последнего символа в строке (поскольку индексы в Python начинаются с 0), и -1 является индексом, следующим за первым, что позволяет включить в последовательность и 0. Шаг -1 указывает, что каждая следующая итерация должна происходить в обратном порядке.
- 'print(message[i])' : Здесь каждый символ строки message выводится по одному, начиная с конца и идя к началу.
- Исходное сообщение выводится в обратном порядке одним символом на каждой строке.
  
## Самостоятельная работа №3
- Напишите программу, которая будет выводить текущее время, с 
точностью до секунд на протяжении 5 секунд. Программу нужно написать с использованием цикла. Подсказка: необходимо 
использовать модуль datetime и time, а также вам необходимо как-то “усыплять” программу на 1 секунду.
### Код
```python
value = int(input("Введите число от 0 до 10: "))
if value < 0 or value > 10:
    print("Введенное значение не находится в диапазоне от 0 до 10")
    exit()
elif value <= 3:
    print("Число находится в диапазоне от 0 до 3")
elif value < 10:
    print("Число находится в диапазоне от 3 до 10")
else:
    print("Число находится в диапазоне от 10")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_2.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_3.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_4.png)
### Выводы:
- Запрашивается ввод числа от пользователя в диапазоне от 0 до 10.
- Если введенное значение меньше 0 или больше 10, выводится сообщение "Введенное значение не находится в диапазоне от 0 до 10", а затем программа завершается.
- Иначе, если значение меньше или равно 3, выводится сообщение "Число находится в диапазоне от 0 до 3".
- Иначе, если значение меньше 10, выводится сообщение "Число находится в диапазоне от 3 до 10".
- Иначе (если значение равно 10), выводится сообщение "Число находится в диапазоне от 10".
  
## Самостоятельная работа №4
- Напишите программу, которая считает среднее арифметическое от аргументов вызываемое функции, с условием того, что изначальное количество этих аргументов неизвестно. Программу необходимо
реализовать используя одну функцию и “точку входа”.
### Код
```python
sentence = input('Введите предложение: ')
length = len(sentence)
print("Длина предложения:", length)
lower_case = sentence.lower() # Перевод предложения в нижний регистр
print("Предложение в нижнем регистре:", lower_case)
vowels = ['a', 'e', 'i', 'o', 'u']
vowel_count = 0
for char in sentence:
        if char.lower() in vowels:
                vowel_count += 1
print("Количество гласных в предложении:", vowel_count) # Подсчет количества гласных
replaced_sentence = sentence.replace("ugly", "beauty")
print("Предложение с замененными словами:", replaced_sentence) # Замена слова "ugly" на # "beauty"
starts_with_the = sentence.startswith("The")
ends_with_end = sentence.endswith("end")
print("Начинается ли предложение с 'The':", starts_with_the)
print("Заканчивается ли предложение на 'end':", ends_with_end) # Проверка начала
# предложения с "The" и окончания на "end"
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I4_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I4_2.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I4_3.png)
### Выводы:
- Код определяет длину предложения, используя встроенную функцию len(). Эта количество символов в предложении.
- Приводит все символы предложения к нижнему регистру с помощью метода .lower().
- Подсчитывает количество гласных букв в предложении. Цикл for проходит по каждому символу в предложении и, если этот символ присутствует в списке гласных (vowels), увеличивает счетчик вхождения гласных (vowel_count).
- Заменяет все вхождения слова "ugly" на слово "beauty" в предложении с помощью метода .replace().
- Проверяет, начинается ли предложение со слова "The" и заканчивается ли оно словом "end". Для этого используются методы строки .startswith() и .endswith().
  
## Самостоятельная работа №5
- Создайте два Python файла, в одном будет выполняться вычисление площади треугольника при помощи формулы Герона (необходимо реализовать через функцию), а во втором будет происходить 
взаимодействие с пользователем (получение всей необходимой информации и вывод результатов). Напишите эту программу и выведите в консоль полученную площадь.
### Код
```python
memory = ' world'
string = 'hello'
counter = 0
values = [0, 2, 4, 6, 8, 10]
while counter != 10:
    if counter in values:
        print(string + memory)
        print(string)
    counter += 1
string = string + ' world'
memory = string
print(memory)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I5.png)
### Выводы:
- Создание строковых переменных memory и string со значениями ' world' и 'hello' соответственно.
-  Создание числовой переменной counter со значением 0 и список values, который содержит значения от 0 до 10 с шагом 2.
- Затем начинается цикл while, который будет выполняться до тех пор, пока counter не станет равным 10.
- Внутри цикла проверка, является ли текущее значение переменной counter одним из значений в списке values. Если значение counter присутствует в values, то на экран выводятся две строки: соединение строк string и memory, а затем просто string. Если значение counter отсутствует в списке values, цикл просто продолжается без действий.
- После проверки значение counter увеличивается на 1 каждый проход цикла.
- Когда цикл завершается (это случится когда counter станет равным 10), происходит соединение строк string и memory, результат которого записывается обратно в string.
- Значение string присваивается переменной memory.
- В конце вы выводите содержимое переменной memory, которая в этот момент будет содержать 'hello world'.

## Общие выводы по теме
- Операторы, условия и циклы в Python являются мощными инструментами, которые позволяют создавать гибкие и эффективные алгоритмы. 
