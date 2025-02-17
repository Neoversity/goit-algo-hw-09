# Видача Решти: Жадібний Алгоритм та Динамічне Програмування

## Опис

Це домашнє завдання охоплює два підходи до проблеми видачі решти: жадібний алгоритм та динамічне програмування. Ми реалізували обидва методи і порівняли їх ефективність.

## Реалізовані Функції

1. **Жадібний Алгоритм**
   - Функція: `find_coins_greedy(amount)`
   - Принцип роботи: Спочатку вибираються найбільші доступні номінали монет для формування суми.
   - Переваги: Швидкий та простий у реалізації.
   - Недоліки: Не завжди знаходить оптимальне рішення.

2. **Динамічне Програмування**
   - Функція: `find_min_coins(amount)`
   - Принцип роботи: Використовує динамічне програмування для знаходження мінімальної кількості монет.
   - Переваги: Завжди знаходить оптимальне рішення.
   - Недоліки: Більш складний та повільніший у виконанні для великих сум.

## Висновки

### Жадібний Алгоритм

Жадібний алгоритм має часову складність O(n), де n - кількість різних номіналів монет. Він дуже швидкий і ефективний для практичного використання, особливо коли набір монет обмежений. Наприклад, для суми 113 він повертає результат {50: 2, 10: 1, 2: 1, 1: 1}. Однак, цей алгоритм не гарантує оптимального рішення для всіх можливих наборів номіналів монет.

### Динамічне Програмування

Алгоритм динамічного програмування має часову складність O(n * amount), де n - кількість різних номіналів монет, а amount - сума, яку необхідно розбити. Цей алгоритм завжди знаходить оптимальне рішення, використовуючи мінімальну кількість монет. Для суми 113 він повертає результат {1: 1, 2: 1, 10: 1, 50: 2}, що є оптимальним розв'язком. Однак, цей підхід може бути більш повільним для великих сум через його обчислювальну складність.

### Порівняння

- **Швидкість**: Жадібний алгоритм працює швидше завдяки своїй простоті.
- **Оптимальність**: Алгоритм динамічного програмування завжди знаходить оптимальне рішення.
- **Використання**: Жадібний алгоритм підходить для випадків, коли швидкість важливіша за оптимальність, а динамічне програмування - для ситуацій, де важлива оптимальність рішення.

## Використання

Запустіть файл `main.py`, щоб протестувати алгоритми. Ви можете вибрати алгоритм для видачі решти та ввести суму для розбиття на монети.

```sh
python main.py
