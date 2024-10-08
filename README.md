1. Функция fibonacci(n)

def fibonacci(n):
    fib_sequence = [0, 1]
    for i in range(2, n * (n + 1) // 2):  # Достаточно для создания пирамиды
        fib_sequence.append(fib_sequence[-1] + fib_sequence[-2])
    return fib_sequence


- Назначение: Эта функция генерирует последовательность чисел Фибоначчи.
- Аргумент: n — количество строк, которое будет использовано для построения пирамиды.
- Логика:
  - Начальная последовательность инициализируется с первых двух числа Фибоначчи: 0 и 1.
  - Цикл for добавляет новые числа в последовательность, пока не будет достигнуто количество, необходимое для построения пирамиды. Количество элементов в последовательности определяется формулой \\( n \\times (n + 1) / 2 \\), так как для n строк пирамиды потребуется \\( \\frac{n(n+1)}{2} \\) чисел.
- Возвращаемое значение: Возвращает список чисел Фибоначчи.

▎2. Функция print_fibonacci_pyramid(rows)

def print_fibonacci_pyramid(rows):
    fib_sequence = fibonacci(rows)
    index = 0
    
    for i in range(1, rows + 1):
        # Печатаем пробелы для выравнивания
        print(" " * (rows - i), end='')
        for j in range(i):
            print(fib_sequence[index], end=' ')
            index += 1
        print()  # Переход на новую строку


- Назначение: Эта функция выводит на экран пирамиду из чисел Фибоначчи.
- Аргумент: rows — количество строк в пирамиде.
- Логика:
  - Сначала вызывается функция fibonacci, чтобы получить последовательность чисел Фибоначчи.
  - Внешний цикл проходит от 1 до rows, где i — текущий номер строки.
  - Внутренний цикл печатает числа Фибоначчи в текущей строке. Для этого используется переменная index, чтобы отслеживать текущее число в последовательности.
  - Перед печатью каждого числа добавляются пробелы для выравнивания, чтобы пирамида выглядела правильно.
- Вывод: Пирамида чисел Фибоначчи отображается в консоли.

▎3. Функция factorial(n)

def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)


- Назначение: Эта рекурсивная функция вычисляет факториал заданного числа.
- Аргумент: n — число, факториал которого нужно вычислить.
- Логика:
  - Если n равно 0 или 1, возвращается 1 (по определению факториала).
  - В противном случае функция вызывает саму себя, умножая n на факториал числа n-1.
- Возвращаемое значение: Возвращает факториал числа n.

▎Заключение

# Добавьте вызов функции в конец файла
print(f"Факториал числа {rows}: {factorial(rows)}")
# Укажите количество строк пирамиды
rows = 24
print_fibonacci_pyramid(rows)


- В этом коде задается переменная rows, которая определяет количество строк в пирамиде (в данном случае 24).
- Затем вызывается функция print_fibonacci_pyramid, чтобы вывести пирамиду чисел Фибоначчи.
- После этого выводится факториал числа rows, используя функцию factorial.
