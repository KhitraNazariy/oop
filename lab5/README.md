# Звіт до роботи lab5

## Тема: Знайомство з ООП

### Мета: Навчитись працювати з класама та об'єктами

---

### Виконання роботи:

- Розробив/Створив обєкти та класи, спробували методи, класові змінні та класові методи, попрацювали з атрибутами...

<details><summary> >>>>>> Python Code <<<<<< </summary>
### Перша програма на ООП

```python
class MyName:
    """Опис класу / Документація
    """
    total_names = 0  # Class Variable

    def __init__(self, name=None) -> None:
        # Class attributes / Instance variables
        self.name = name if name is not None else self.anonymous_user().name
        MyName.total_names += 1  # modify class variable
        self.my_id = self.total_names

    @property
    def whoami(self):
        """Class property
        return: повертаємо імя 
        """
        return f"My name is {self.name}"

    @property
    def my_email(self) -> str:
        """Class property
        return: повертаємо емейл
        """
        return self.create_email()

    def create_email(self) -> str:
        """Instance method
        """
        return f"{self.name}@itcollege.lviv.ua"

    @classmethod
    def anonymous_user(cls):
        """Classs method
        """
        return cls("Anonymous")

    @staticmethod
    def say_hello(message="Hello to everyone!"):
        """Static method
        """
        return f"You say: {message}"

    def name_length(self):
        return len(self.name)


print("Let's Start!")

names = ("Nazar", "Artur", None,)
all_names = {name: MyName(name) for name in names}

for name, me in all_names.items():
    print(f"""\n{">*<"*20}
This is object: {me} 
This is object attribute: {me.name} / {me.my_id}
This is {type(MyName.whoami)}: {me.whoami} / {me.my_email}
This is {type(me.create_email)} call: {me.create_email()}
This is static {type(MyName.say_hello)} with defaults: {me.say_hello("aaaaaaa")} 
This is class variable {type(MyName.total_names)}: from class {MyName.total_names} / from object {me.total_names}
Lenght name = {me.name_length()}
We are done. We create {me.total_names} names! ??? Why {MyName.total_names}?
{"<*>"*20}
""")

print(
    f"We are done. We create {me.total_names} names! ??? Why {MyName.total_names}?")
```

</details>

 - результат

```
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000018F0E36BB50> 
This is object attribute: Nazar / 1
This is <class 'property'>: My name is Nazar / Nazar@itcollege.lviv.ua
This is <class 'method'> call: Nazar@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: aaaaaaa 
This is class variable <class 'int'>: from class 4 / from object 4
Lenght name = 5
We are done. We create 4 names! ??? Why 4?
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>


>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000018F0E36BAF0> 
This is object attribute: Artur / 2
This is <class 'property'>: My name is Artur / Artur@itcollege.lviv.ua
This is <class 'method'> call: Artur@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: aaaaaaa 
This is class variable <class 'int'>: from class 4 / from object 4
Lenght name = 5
We are done. We create 4 names! ??? Why 4?
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>


>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000018F0E36BA90>
This is object attribute: Anonymous / 4
This is <class 'property'>: My name is Anonymous / Anonymous@itcollege.lviv.ua
This is <class 'method'> call: Anonymous@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: aaaaaaa
This is class variable <class 'int'>: from class 4 / from object 4
Lenght name = 9
We are done. We create 4 names! ??? Why 4?
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>

We are done. We create 4 names! ??? Why 4?
```

- Відповіді на запитання:

1. Чому коли передаємо значення None створюється обєкт з іменем Anonymous?

   - бо в класі є метод який повертає Anonymous якщо ім'я = none

   ```py
    def anonymous_user(cls):
        """Classs method
        """
        return cls("Anonymous")
   ```

2. Як змінити текст привітання при виклику методу say_hello()? Допишіть цю частину коду.

   - me.say_hello("some text") <- можна написати текст у виклик функції. Якщо робити виклик без параметрів то метод поверне "Hello to everyone!"

3. Допишіть функцію в класі яка порахує кількість букв в імені (підказка: використайте функцію len());

   - це було просто:

   ```py
   def name_lenght(self):
        return len(self.name)
   ```

### Висновок:

## На даній лабораторній роботі я навчився працювати з класама та об'єктами