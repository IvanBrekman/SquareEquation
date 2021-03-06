# SolveSquareEquations

Данный проект предоставляет функции для решения квадратных уравнений

В данном модуле содержится:
* main.c - файл выполняет тестирование и приглашает пользователя на ввод коэффициентов для решения уравнения
* test.c - файл содержит функции для тестирования программы
* solve_equation.c - файл, содержащий всю логику модуля

### Основная функция модуля solve_square_equation
Данная функция принимает 5 аргументов:
* double a - коэффициент при x**2
* double b - коэффициент при x
* double c - свободный коэффициент
* double solve1 - указатель на переменную, в которую будет записан 1 ответ**
* double solve2 - указатель на переменную, в которую будет записан 2 ответ

Функция имеет возвращаемое значение типа int: количество решений***

При некорректном вводе программа вернет код -2 (код ошибки записывается в errno)

### Примечания:
** - Если у уравнения 1 ответ, то его значение продублируется в solve2

*** - Если у уравнения бесконечно много решений, то функция вернет -1

### Функция для решения линейного уравнения "solve_linear_equation"
Сигнатура этой функции схожа с solve_square_equation. Она применяется в указанной функции в случае вырожденного квадратного уравнения (а == 0). При необходимости Вы можете пользоваться этой функцией также, как и solve_square_equation

### Функция для сравнения числа с 0 "is_zero"
Так как операции с double имеют некоторую погрешность, то в модуле используется функция, сравнивающая число с 0, учитывая эту погрешность
