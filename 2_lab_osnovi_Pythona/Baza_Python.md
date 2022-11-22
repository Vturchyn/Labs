#               *МІНІСТЕРСТВО ОСВІТИ І НАУКИ*
#       *ВСП " ФАХОВИЙ КОЛЕДЖ ІНФОРМАЦІЙНИХ ТЕХНОЛОГІЙ "*
#                *НУ ЛЬВІВСЬКА ПОЛІТЕХНІКА*

![alt text](https://github.com/Vturchyn/Labs/blob/c00754d8ec38288fd662ce6ce98ddfac22916db7/1_lab_python_program/%D1%84%D0%BE%D1%82%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D1%96%D1%97/logotype.jpg "logotype of ІТ Коледж")


---
##             *Звіт до лабораторної роботи 2*

###### з дисципліни об'єктовно-орієнтоване програмування
######              студента групи _ТК-330_
######                 _Турчина Віталія_
######             Перевірив: _Богдан Бугиль_

### _Тема: Основи програмування на Python_
### _Мета роботи: Навчитись основним основам програмування на Путхоні_


---
### **Виконання роботи** / **Хід роботи**

### Основні конструкції в Путхон

1. Створив Путхон файл `*.пу` або `.iпуnb` в якому виконував базові приклади. Застосовуючи команду `print` виконав наступне:

    1. Познайомився з основними [типами даних](https://docs.python.org/3.10/library/stdtypes.html#numeric-types-int-float-complex). Попракитикував з простими змінними, списками `list`, наборами `set` та словниками `dict`:

```python
String  = 'riadok'
Integer = 0
List    = ['a', 1, 2, 3, 'Слово']
Dict    = {'a': 1, 'b': 2}
Set     = ('a', 'b', 'c',)

print (f' це рядок      -> {String}')
print (f' це ціле число -> {Integer}')
print (f' це список     -> {List}')
print (f' це словник    -> {Dict}')
print (f' це набір      -> {Set}')
```

```python
 це рядок      ->    riadok
 це ціле число ->    0
 це список     ->    ['a', 1, 2, 3, 'Слово']
 це словник    ->    {'a': 1, 'b': 2}
 це набір      ->    ('a', 'b', 'c')
```

   1. Вивів [вбудовані константи](https://docs.python.org/3.10/library/constants.html), (2-3 на вибір), наприклад:
    
```python
print (True)
print (False)
print (None)
print (NotImplemented)
```

```python
True
False
None
NotImplemented
```

   1. Вивів результат роботи [вбудованих функцій](https://docs.python.org/3.10/library/functions.html#func-repr) (2-3 на вибір), наприклад:

```python
print(abs(-11.1), f "є рівним {abs(11.1)}")
```

```python
print(bin(1), f "не є рівним {format(1, 'b')}")
```


   1. Познайомився з [циклами](https://docs.python.org/3.10/reference/compound_stmts.html#the-for-statement). Написав будь-який код який демонструє роботу циклів, (2-3 на вибір), наприклад:

```python

num = 1000
while num > 0:
    print (f'{num} - 7 = {num-7}')
    num -= 7
```

```python
1000 - 7 = 993
...
6    - 7 = -1
```

   1. Познайомився з [розгалуженнями](https://docs.python.org/3.10/reference/compound_stmts.html#the-if-statement). Написав будь-який код який демонструє роботу розгалужень, (2-3 на вибір), наприклад:
    
```python
     A = True
print ( " Значить А = True" if A else " Значить А=False " )

choise = input(">>> ")
match choise:
    case '1':
        print('вибір 1')

    case 'провірка':
        print('вибір провірки')

    case _:
        print('ви пацифіст')
```

```python
Значить А = True
ви пацифіст
```
       
   1. Конструкція `try`->`except`->`finally`. У мові Путхон код не компілюється, а виконується відразу. Можливі помилки виловлювив сам. Написав свій варіант коду з помилкою. Наприклад:
       
```python
A = 0
B = 0
try:
    print("Компілюй код", B/A, "!")
except Exception as e:
    print(e)
finally:
    print("Сам такий!")
```
       
   1. Контекст-менеджер `with`. Міг і почитатив [тут](https://python-scripts.com/contextlib). Написав свій код з контекст-менеджером, наприклад:
  
```python
       with open("riadochki.md", "r") as f:
    for line in f:
        print(line)
```

```python
riadochok 1

riadochok drugiy

tretiy nah..
```
       
   1. Познайомився з Путхоном [lambdas](https://docs.python.org/3.10/reference/expressions.html#lambda). Написав свій приклад коду так як я розумів Лямбди, наприклад:
      
```python
this_is_lambda_dude = lambda first, last: f'Зис код врайте: {first} {last}'
print("іт зис фанкшинс, чувак:", this_is_lambda_dude)
print("Зис хер call:", this_is_lambda_dude('Віталій', 'Турчин'))
```

```python
sqrt = lambda x: x**0.5
print("іт зис фанкшинс,чувак:", sqrt)
print(f'квадратний корінь 9 = {sqrt(9)}')
```

```python
Зис фанкшинс, чувак: <function <lambda> at 0x000001A381135000>
квадратний корінь 9 = 3.0
```

---
### **Висновок**: 
> Під час виконання лабораторної роботи я досягнув мети роботи, а саме навчився основним основам програмування на Путхоні. 
