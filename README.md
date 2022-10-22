Collatz Conjecture (3n+1 problem) Iterator
----------------------------

### Условия
0. Задано натуральное число `N`.
1. Если `N` - чётное, то `N = N / 2`;
2. Если `N` - нечётное, то `N = 3 * N + 1`;
3. Вернуться к шагу 1.

### Гипотеза
Гипотеза гласит, что все числа сводятся к циклу `4 -> 2 -> 1`.
Или, иными словами, гипотеза заключается в том, что какое бы начальное число `N` мы ни взяли, рано или поздно мы получим единицу.
Доказать или опровергнуть математики на данный момент эту гипотезу не могут.

Я ничего доказывать тоже не буду, ибо не математик, а просто сделаю простенький
итератор на Rust, который будет инициализироваться числом `N` и возвращать следующий
элемент согласно заданным условиям.

### Ограничения
Используется `u128` из примитивных типов Rust.
Соответственно, работу с отрицательными числами я не рассматриваю.

Ну и работать с числами больше `2^128` тоже не получится.
Если вдруг в процессе подсчётов произойдёт переполнение `u128`, то итератор вернёт `None`.

## Лицензия
`SPDX-License-Identifier: MIT OR Apache-2.0`
