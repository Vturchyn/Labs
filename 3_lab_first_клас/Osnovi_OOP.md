#               *МІНІСТЕРСТВО ОСВІТИ І НАУКИ*
#       *ВСП " ФАХОВИЙ КОЛЕДЖ ІНФОРМАЦІЙНИХ ТЕХНОЛОГІЙ "*
#                *НУ ЛЬВІВСЬКА ПОЛІТЕХНІКА*

![alt text](https://github.com/Vturchyn/Labs/blob/c00754d8ec38288fd662ce6ce98ddfac22916db7/1_lab_python_program/%D1%84%D0%BE%D1%82%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D1%96%D1%97/logotype.jpg "logotype of ІТ Коледж")


---
##             *Звіт до лабораторної роботи 3*

###### з дисципліни об'єктовно-орієнтоване програмування
######              студента групи _ТК-330_
######                 _Турчина Віталія_
######             Перевірив: _Богдан Бугиль_

### _Тема: Основи ООП_
### _Мета роботи: Знайомство з ООП_


---
### **Виконання роботи** / **Хід роботи**

# Знайомство з ООП

### Створив перший class
1. Створив два python файли: для Ноутбука з розширенням `.ipynb` та для скрипта з розширенням `.py`;
1. Скопіюйвав Python код наведений внизу у Ваші файли та виконайте їх натиснувши `Run Python File` (трикутник з трьома кутами); 

<details><summary> >>>>>> Python Code <<<<<< </summary>

### Перша програма на ООП
```python

class MyName:
    """Опис класу / Документація
    """
    total_names = 0 #Class Variable

    def __init__(self, name=None) -> None:
        self.name = name if name is not None else self.anonymous_user().name #Class attributes / Instance variables
        MyName.total_names += 1 #modify class variable
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


print("Let's Start!")

names = ("Bohdan", "Marta", None)
all_names = {name: MyName(name) for name in names}

for name, me in all_names.items():
    print(f"""{">*<"*20}
This is object: {me} 
This is object attribute: {me.name} / {me.my_id}
This is {type(MyName.whoami)}: {me.whoami} / {me.my_email}
This is {type(me.create_email)} call: {me.create_email()}
This is static {type(MyName.say_hello)} with defaults: {me.say_hello()} 
This is class variable {type(MyName.total_names)}: from class {MyName.total_names} / from object {me.total_names}
{"<*>"*20}""")

print(f"We are done. We create {me.total_names} names! ??? Why {MyName.total_names}?")

```
</details>

1. Вказав у звіті що вивела пограма або не зробив скріншот та тимбільш не вставив у звіт:

```
This is object: <__main__.MyName object at 0x000001928467ADD0>
This is object attribute: Bohdan / 1
This is <class 'property'>: My name is Bohdan / Bohdan@itcollege.lviv.ua
This is <class 'method'> call: Bohdan@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone!
This is class variable <class 'int'>: from class 5 / from object 5

This is object: <__main__.MyName object at 0x0000019284679D20>
This is object attribute: Marta / 2
This is <class 'property'>: My name is 3sentiabriaikalendarpereverny / 3sentiabriaikalendarpereverny@itcollege.lviv.ua
This is <class 'method'> call: 3sentiabriaikalendarpereverny@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone!
This is class variable <class 'int'>: from class 5 / from object 5

This is object: <__main__.MyName object at 0x0000019284679C00>
This is object attribute: Anonymous / 4
This is <class 'property'>: My name is Anonymous / Anonymous@itcollege.lviv.ua
This is <class 'method'> call: Anonymous@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone!
This is class variable <class 'int'>: from class 5 / from object 5

This is object: <__main__.MyName object at 0x00000192846D49C0>
This is object attribute: Vitaliy / 5
This is <class 'property'>: My name is Vitaliy / Vitaliy@itcollege.lviv.ua
This is <class 'method'> call: Vitaliy@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone!
This is class variable <class 'int'>: from class 5 / from object 5

We are done. We create 5 names! ??? Why 5?

```

3. Ознайомився з кодом та прозрів в чому сенс життя та, також, за що відповідає кожен з рядків;
4. Модифікував програму додавши своє імя в список;
5. Дав відповідь на запитання: 
    - Чому коли передаємо значення `None` створюється обєкт з іменем `Anonymous`?
    > Заміняє відсутність значення що і являю собою значення "None" (пустота, ніц) на слово "Anonymous" (безіменний). Це прописано в коді.
    - Як змінити текст привітання при виклику методу `say_hello()`? Допишіть цю частину коду.
    > Щось в нього вписати: say_Hello("нє")
    - Допишіть функцію в класі яка порахує кількість букв і імені (підказка: використайте функцію `len()`);
    >   
   ```py tyhon
    print(len(name)-(len(name)+name.count('і')
    (підсказка: в слові імені їх дві)
   ```
   
    - Порахуйте кількість імен у списку `names` та порівняйте із виведеним результатом. Дайте відповідь чому маємо різну кількість імен?
    > Програма нас на'обує конкретно. За далба'обів м'ягкокажучи тримає (конкретних). Третя версія - менш ймовірна но все ж вона існує така ймовірність - анонімуси тоже люди і з ними теж треба рахуватись і не раз.
    
    > P.S. одна версія не виключає наявності другої.

---


### **Висновок**: 
> Під час виконання лабораторної роботи я досягнув мети роботи, а саме ознайомився з ООП. 
