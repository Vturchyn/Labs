#               *МІНІСТЕРСТВО ОСВІТИ І НАУКИ*
#       *ВСП " ФАХОВИЙ КОЛЕДЖ ІНФОРМАЦІЙНИХ ТЕХНОЛОГІЙ "*
#                *НУ ЛЬВІВСЬКА ПОЛІТЕХНІКА*

![alt text](https://github.com/Vturchyn/Labs/blob/c00754d8ec38288fd662ce6ce98ddfac22916db7/1_lab_python_program/%D1%84%D0%BE%D1%82%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D1%96%D1%97/logotype.jpg "logotype of ІТ Коледж")


---
##             *Звіт до лабораторної роботи 5*

###### з дисципліни об'єктовно-орієнтоване програмування
######              студента групи _ТК-330_
######                 _Турчина Віталія_
######             Перевірив: _Богдан Бугиль_

### _Тема: Тестування програм_
### _Мета роботи: Проестувати програми_


---
### **Виконання роботи** / **Хід роботи**

# Тестування
> Це процес перевірки правильності роботи програм, їх функцій та поведінки при різних умовах роботи шляхом створення штучних ситуацій або сценаріїв.  
1. Для роботи нам буде потрібно створити декілька Python файлів. 
---

### Перевірив assert
1. `assert` - це перевірка певних тверджень та встановлення працездатності коду. Твердження дозволяють перевірити правильність коду, перевіряючи, чи виконуються певні умови.
    ```python
    number = -1
    assert number > 0, "число має бути більшим за нуль!"
    ```
1. Створив власний крок `assert` та зробив тестові превірки при введенні даних з клавіатури. Для цього використав метод `input` як показано нижче:
    ```python
    a = input("Введіть число: ")
    assert a.isdigit(), "Потрібно ввести число!"
    print(f"введене число: {a}")
    ```
2. В ООП методи `assert` найкраще виконувати для перевірки (валідації) правильності вводу аргументів. Для прикладу маємо простий клас в якому здійснюємо валідацію даних перед тим як створювати обєкт. Умовою валідації може бути будь-який вираз Python який повертає значення True/False.
    ```python
    class Figure:
        def __init__(self, type, length) -> None:
            assert length > 0, "Довжина має бути більшою за 0!"
            assert type in ["квадрат", "прямокутник", "трикутник"], "Дозволені фігури: квадрат, прямокутник, трикутник"
            self.type = type
            self.length = length

    #a = Figure("трапеція", 12)
    #b = Figure("квадрат", 0)
    c = Figure("квадрат", 1)
    ```
3. Виконав код наведений вище для різних обєктів. Вставив у звіт результат виконання роботи для різної комбінації введених значень при створенні обєкта:
   -
```python
chislo = input('Введіть число -> ')
assert chislo.isdigit(), f'Задзвоніть за номером нище...'

name = input(
    'Введіть Username -> ')

list = name.split()
for item in list:
    assert item.istitle(), f'Ти шо забув де капслок з шифтом чи зір підводить? Рішення завжди є - дзвони по номеру вказаному нище.'

print(f'Прийміть наші співчуття {name}, ви ввели {chislo} )
```

```
Введіть число -> 666
Введіть username (через пробіл, з великої літери) -> Dopustim
Прийміть наші співчуттяm, Dopustim, ви ввели 666
```

```
Введіть число -> не число
AssertionError: Задзвоніть за номером нище https://micto.ua/lvivska-oblasna-klinichna-psykhiatrychna-likarnia-i158965/
```

```
Введіть число -> 666
Введіть username (з великої літери) -> dopustim
AssertionError: Ти шо забув де капслок з шифтом чи зір підводить? Рішення завжди є - дзвони по номеру вказаному вище.
```

```
class Figure:
    def __init__(self, type, length) -> None:
        assert length > 0, "Довжина має бути більшою за 0!"
        assert type in ["квадрат", "прямокутник",
                        "трикутник"], "Дозволені фігури: квадрат, прямокутник, трикутник"

        self.type = type
        self.length = length

    def print_figure(self):
        return f'Фігура {self.type} з cтороною {self.length}'


try:
    figure1 = Figure("квадрат", 4)
    print(f'Фігура 1 - {figure1.print_figure()}')
except AssertionError as err:
    print(f'Фігура 1 - {err}')

try:
    figure2 = Figure("прямокутник", 0)
    print(f'Фігура 2 - {figure2.print_figure()}')
except AssertionError as err:
    print(f'Фігура 2 - {err}')

try:
    figure3 = Figure("трикутник", -666)
    print(f'Фігура 3 - {figure3.print_figure()}')
except AssertionError as err:
    print(f'Фігура 3 - {err}')

try:
    figure4 = Figure("трикутник", 22)
    print(f'Фігура 4 - {figure4.print_figure()}')
except AssertionError as err:
    print(f'Фігура 4 - {err}')

try:
    figure5 = Figure("трапеція", 100)
    print(f'Фігура 5 - {figure5.print_figure()}')
except AssertionError as err:
    print(f'Фігура 5 - {err}')

```

```
Фігура 1 - Фігура квадрат з cтороною 4
Фігура 2 - Довжина має бути більшою за 0!
Фігура 3 - Довжина має бути більшою за 0!
Фігура 4 - Фігура трикутник з cтороною 22
Фігура 5 - Можливі фігури: квадрат, прямокутник, трикутник
```

```
class Name:
    def __init__(self, name, hobby='') -> None:
        if name not in ["Богдан", "Dopustim", "Анонім"]:
            raise ValueError("Дозволені імена: Богдан, Анонім")
        if hobby == '':
            raise ValueError("Ти шо?")

        self.name = name
        self.hobby = hobby


a = Name("Dopustim", "допускати")
b = Name("Dopustim")
```

```
Traceback (most recent call last):
  File "E:\Labs\5_lab\testing.py", line 13, in <module>
    b = Name("Dopustim")
  File "E:\Labs\5_lab\testing.py", line 6, in __init__
    raise ValueError("Ти шо?")
ValueError: Ти шо?
```
5. 
    ```python
    class Name:
        def __init__(self, name) -> None:
            if name not in ["Богдан", "Анонім"]:
                raise ValueError("Дозволені імена: Богдан, Анонім")
            self.name = name

    a = Name("dopustim")
    ```
5. 
---

### Юніт тести
> Це перевірка малої частини коду, юніта. Найчастіше це порівняння між введеними даними та результатом виконання якоїсь частини програми.
1. Найпростіше використовувати вбудовану бібліотеку для юніт тестів `unittest`. Зазвичай юніт тести створюються в окремому файлі, однак в межах проекту який має бути протестованим.
1. Створив простий клас з двома пропертями, та навмисно зробив помилку в ньому. Для коректної роботи з тестами назвіть файл `app.py`. Це буди потрібно для імпорту бібліотек (класів).
    ```python
    class Figure:
        FIGURES = ["квадрат", "прямокутник", "трикутник"]
        def __init__(self, type, length) -> None:
            assert length > 0, "Довжина має бути більшою за 0!"
            assert type in self.FIGURES, "Дозволені фігури: квадрат, прямокутник, трикутник"
            self.type = type
            self.length = length

        @property
        def get_figure_type(self):
            return self.type

        @property
        def get_figure_length(self):
            return self.type # робимо помилку
    ```
2. Спробував застосувати цей клас та створив декілька обєктів, викликав методи пропертіс. 
3. Створив юніт тести та спробував перевірити тестовий клас щоб все працювало правильно. Для цьго у методі `setUp` з допомогою бібліотеки `random` створимо обєкт та перевірив чи правильно працюють методи:
    ```python
    import unittest
    from random import choice, randint

    from app import Figure # назва файлу з нашим класом повинна бути app.py

    class TestFigure(unittest.TestCase):
        @classmethod
        def setUpClass(cls):
            """Виконається лише раз на початку тестів
            """
            pass
        
        def setUp(self) -> None:
            """Виконується кожного разу коли запускається тест
            """
            self.figure = choice(Figure.FIGURES)
            self.length = randint(1, 10)
            self.obj = Figure(self.figure, self.length)
            return super().setUp()

        def tearDown(self) -> None:
            del self.obj
            return super().tearDown()

        def test_figure_type(self):
            print(f"Тестуємо вивід, має бути: {self.figure} == {self.obj.get_figure_type}")
            self.assertEqual(self.figure, self.obj.get_figure_type, "Властивість get_figure_type повертає непривильну фігуру!")

        def test_figure_lengh(self):
            self.assertEqual(self.length, self.obj.get_figure_length, "Властивість get_figure_length повертає непривильну довжину!")
        
        def test_obj(self):
            with self.assertRaises(AssertionError):
                Figure("коло", 1) # Спробував створити обєкт з недозволеними параметрими, в нас є помилка AssertionError


    if __name__ == '__main__':
        unittest.main() # unittest.main(verbosity=2) щоб був більш детальний вивід
    ```
4. Виконав тести двома способами:
   1. Якщо у програмі є блок з викликом бібліотеки `unittest.main()`, то програму викликав з Visual Studio Code через кнопку `Run` (трикутник :arrow_forward:) або який регулярний Python файл:
   ```bash
   python test.py
   ```
   1. Викликав напряму з консолі (немає запуску `unittest.main()`), виконав команду з явним викликом бібліотеки `unittest`. Для більш детального виводу просто додайте опцію `-v` або `--verbose`:
   ```bash
   python -m unittest
   ```
5. Попрактикувався викликати тести з консолі та з Visual Studio Code. Вказав які тести виконуються а які провалюються:
   -
```
test_figure_color (__main__.TestFigure) ... ok
test_figure_lengh (__main__.TestFigure) ... FAIL
test_figure_type (__main__.TestFigure) ... Тестуємо вивід, має бути: прямокутник == прямокутник
ok
test_obj (__main__.TestFigure) ... ok

======================================================================
FAIL: test_figure_lengh (__main__.TestFigure)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "E:\Labs\5_lab\Testing.py", line 33, in test_figure_lengh
    self.assertEqual(self.length, self.obj.get_figure_length,
AssertionError: 5 != 'прямокутник' : Властивість get_figure_length повертає непривильну довжину!

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (failures=1)
```

7. При виконанні юніт тестів зявилась папка `__pycache__` яку не комітив в репозиторій, тому додав її в `.gitignore`.
8. Розширив функціонал класу який тестується та створив юніт тест для перевірки правильності роботи доданого функціоналу.
---

### Юніт тести з використання бібліотеки PyTest

> PyTest це стороння бібліотета для тестування коду

1. Більш докладно про бібліотеку [PyTest](https://docs.pytest.org/en/7.1.x/) можна прочитати на офіційному сайті. Оскільки, це стороння бібліотека її потрібно інсталювати. Для цього використав віртальні середовища та інструмент `pipenv` (якщо `pipenv` буде некоректно працювати на Windows встановив бібліотеку за допомогою `pip`). Бібліотеки для юніт тестів краще ставити в `--dev` середовище.
    ```bash
    pipenv --python 3.10
    pipenv install pytest --dev
    pipenv install --dev
    ```
2. Дана бібліотека може працювати як з вбудованими тестами які ми вже маємо, так і з будь-якими функціями які розпочинаються з слова `test_`. Для прикладу зробив простий тест та помістимо всередині того ж файлу де і наш клас `Figure`:
    - створив простий тест у файл `app.py`:
    ```python
    def test_app_triangle():
        """Test if we create triangle figure.
        """
        fig = "трикутник"
        triangle = Figure(fig, 4)
        assert triangle.type == fig, f"Фігура має бути {fig}"
    ```
    - запускаємо тести за допомогою `pytest`:
    ```bash
    pipenv run pytest app.py
    ```
3. Вказав у звіті що вивела програма та чи виконалась функція `test_app_triangle`:
   -
```py
def test_app_triangle():
    """Test if we create triangle figure.
    """
    fig = "трикутник"
    len = 4
    col = 'green'

    triangle = Figure(fig, len, col)
    assert triangle.type == fig, f"Фігура має бути {fig}"
```

```
================== test session starts ==================
platform win32 -- Python 3.10.6, pytest-7.1.3, pluggy-1.0.0
rootdir: E:\Labs\github\5_lab
collected 1 item

app.py .              [100%]

================== 1 passed in 0.01s ==================
```
5. Для виклику всіх тестів з файлу `test.py` передав даний файл як аргумент `pytest`:
    ```bash
    pipenv run pytest test.py
    ```
---

### Візуалізація результатів та покриття коду Coverage (pytest-cov)
> Допоміжна бібліотека для збору статистика покриття коду юніт тестами. Покриття тестами - це відношення між кількістю рядків, виконаних хоча б одним тестом, до загальної кількості рядків кодової бази.
1. Можна використовувати бібліотеку [coverage](https://coverage.readthedocs.io/en/6.5.0/) або плагін [pytest-cov](https://pytest-cov.readthedocs.io/en/latest/readme.html).
    - для інсталяції виконав наступні команди:
    ```bash
    pipenv install coverage --dev
    # АБО
    pipenv install pytest-cov --dev
    ```
1. Для виводу покриття коду тестами потрібно або використовувати новий інструмент `coverage` або передавати аргументи у виклик `pytest`.
    - запуска тестів (у репозиторії зявився файл `.coverage`):
    ```bash
    python -m unittest discover
    ```
    - виклик `coverage`:
    ```bash
    pipenv run python -m coverage report
    # АБО
    pipenv run coverage run -m pytest tests.py
    ```
    - виклик через `pytest`. Тут ми передаємо параметр який саме модуль ми хочемо проаналізувати. В даному випадку наша бібліотека з класом знаходиться в файлі `app.py` тому ми передаємо параметр `--cov=app`:
    ```bash
    pipenv run pytest --cov=app test.py
    ```
2. Для візуалізації результаів не в консолі а через браузер - згенеруйте звіт у форматі `html`. Отриманий файл повинен бути у звіті.
    ```bash
    pipenv run python -m coverage html
    ```
---тіпа хаштиемель---
```HTML
Name     Stmts   Miss  Cover
----------------------------
app.py      25      5    80%
----------------------------
TOTAL       25      5    80%
```
--- ©2022. Хаштиемель_Faile.html. Всі права захищені. ---

### **Висновок**: 
> Під час виконання лабораторної роботи я досягнув мети роботи, а саме протестував програми. 

> У висновку відповів на запитання:
- Що зроблено в роботі?
  > В роботі було зроблено тестування програм, Візуалізація результатів та покриття коду Coverage (pytest-cov), юніт тести та перевірка assert.
- Чи досягнуто мети роботи?
  > Так, мета робити в виді тестування програм була досягнута в процесі її виконання.
- Які нові знання отримано?
  > Про тестування програм, візуалізацію результатів, покриття коду Coverage (pytest-cov), юніт тестів та перевірки assert.
- Чи вдалось відповісти на всі питання задані в ході роботи?
  > Надіюсь. 
- Чи вдалося виконати всі завдання?
  > Так, всі завдання було виконано під час виконання роботи по тестуванню програм.
- Чи виникли складності у виконанні завдання?
  > Залежить від того що можна назвати складнощами.
- Чи подобається такий формат здачі роботи (Feedback)?
  > Всеціло і впринципі.
- Побажання для покращення (Suggestions)?
  > Знищення з лиця землі всіх смайликів разом з людьми які їх використовують.
---
