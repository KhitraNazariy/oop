# Основи Python

## Тема: Основні конструкції в Python

### Мета: Навчитись працювати з основними типами даних та функціями в Пайтон 3

---

### Виконання роботи

- Познайомився з основними типами даних. Попракитикувався з простими змінними, списками list, наборами set та словниками dict

```python
str = 'text'
int = 1
list = ['a', 1, 1.25, 'Слово']
dict = {'a': 'Слово', 'b': 1}
set = ('a', 'c', 'b',)

print(f' строка - {str}')
print(f' число - {int}')
print(f' список - {list}')
print(f' словник - {dict}')
print(f' сет - {set}')
```

```
 строка - text
 число - 1
 список - ['a', 1, 1.25, 'Слово']
 словник - {'a': 'Слово', 'b': 1}
 сет - ('a', 'c', 'b')
```

- Вивів дельлька вбудованих констант:

```python
print(True)
print(False)
```

```
True
False
```

- Вбудовані функції

```python
print(abs(-12.5), f"є рівним {abs(12.5)}")
print(round(33.332533, 1))
```

```
12.5 є рівним 12.5
33.3
```

- Цикли

```python
letters = ["a", "b", "c"]
for i in range(len(letters)):
    print(f"На позиції {i} знаходиться буква {letters[i]}")

num = 123
while num > 20:
    print(f'{num} - 22 = {num-22}')
    num-=22
```

```
На позиції 0 знаходиться буква a
На позиції 1 знаходиться буква b
На позиції 2 знаходиться буква c
123 - 22 = 101
101 - 22 = 79
79 - 22 = 57
57 - 22 = 35
35 - 22 = 13
```

- Розгалуження

```python
A = True
print("А=True" if A else "А=False")
A = 5
if A > 5:
    print("Не виконається")
elif A == 1:
    print("Не виконається")
elif A != 2:
    print("Виконається")
else:
    print("гарантовано фолс")
```

```
А=True
Виконається
```

- Конструкція try->except->finally

```py
try:
    print("Що буде якщо", 10/A, "?")
except Exception as e:
    print("Сталася помилка!! =>> ", e)
import random
A = random.choice(["Str", 15, 0])
print(f"Випадковий вибір {A}")
try:
    print("Що буде якщо", 10/A, "?")
    #print(non_exist_variable)\n",
    print("Це без помилок")
except (ZeroDivisionError, NameError, TypeError) as e:
    print("Сталася помилка!! =>> ", e)
finally:
    print("Це виведеться завждиб чи є помилка чи її немає")
```

```
Сталася помилка!!, ми виконали raise
Сталася помилка!! =>>  division by zero
Випадковий вибір Str
Сталася помилка!! =>>  unsupported operand type(s) for /: 'int' and 'str'
Це виведеться завждиб чи є помилка чи її немає
```

- Контекст-менеджер 

```py
with open("TEST.md", "r") as f:
    for line in f:
        print(line)
```

```
test line 1

test line 2

line 3
```

- lambdas

```py
sqrt = lambda x: x**0.5

print("Це просто функція:", sqrt)
print(f'квадратний корінь числа 25 = {sqrt(25)}')
```

```
Це просто функція: <function <lambda> at 0x000001A381135000>
квадратний корінь числа 25 = 5.0
```

### Висновок:

## Я навчився працювати з основними типами даних та функціями в Пайтон 3.