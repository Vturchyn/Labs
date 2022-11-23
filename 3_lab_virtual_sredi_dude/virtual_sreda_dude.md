#               *МІНІСТЕРСТВО ОСВІТИ І НАУКИ*
#       *ВСП " ФАХОВИЙ КОЛЕДЖ ІНФОРМАЦІЙНИХ ТЕХНОЛОГІЙ "*
#                *НУ ЛЬВІВСЬКА ПОЛІТЕХНІКА*

![alt text](https://github.com/Vturchyn/Labs/blob/c00754d8ec38288fd662ce6ce98ddfac22916db7/1_lab_python_program/%D1%84%D0%BE%D1%82%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D1%96%D1%97/logotype.jpg "logotype of ІТ Коледж")


---
##             *Звіт до лабораторної роботи 4*

###### з дисципліни об'єктовно-орієнтоване програмування
######              студента групи _ТК-330_
######                 _Турчина Віталія_
######             Перевірив: _Богдан Бугиль_

### _Тема: Віртуальні середовища_
### _Мета роботи: Проробити роботу у віртуальних середовищах_


---
### **Виконання роботи** / **Хід роботи**

# Віртуальні середовища
> Ізольовані віртуальні середовища - це сукупність Python інтерпретатора, бібліотек та скриптів ізольована від інших інсталяцій.

### Основи роботи з сторонніми бібліотеками

1. Для роботи з сторонніми бібліотеками їх потрібно спочатку встановив. Для їх встановлення є інструмент PIP (`Python Install Package`). Перевірив чи він встановлений на компютері:
    ```bash
    pip -V
    # Після успішного виконання команди виконайте
    pip --help
    ``` 
1. Передивився які дії можна зробити за допомогою `pip`. Перевірив які бібліотеки вже інстальовані на Вашому компютері та вказав їх у звіті (скріншот або стрічки що вивів):
   
<details><summary> === стрічки === </summary>
```<br>
aiogram                   2.16<br>
aiohttp                   3.8.0<br>
aioify                    0.4.0<br>
aiosignal                 1.2.0<br>
altgraph                  0.17.2<br>
anipics                   1.4<br>
appdirs                   1.4.4<br>
arcade                    2.6.9<br>
asgiref                   3.5.2<br>
asttokens                 2.0.8<br>
async-generator           1.10<br>
async-timeout             4.0.1<br>
attrs                     21.2.0<br>
auto-py-to-exe            2.22.0<br>
autopep8                  1.6.0<br>
Babel                     2.9.1<br>
backcall                  0.2.0<br>
beautifulsoup4            4.10.0<br>
bottle                    0.12.19<br>
bottle-websocket          0.2.9<br>
certifi                   2021.10.8<br>
cffi                      1.15.0<br>
cfscrape                  2.1.1<br>
charset-normalizer        2.0.7<br>
click                     8.0.4<br>
click-plugins             1.1.1<br>
colorama                  0.4.4<br>
cryptography              36.0.1<br>
debugpy                   1.6.3<br>
decorator                 5.1.1<br>
Django                    4.0.4<br>
Eel                       0.14.0<br>
entrypoints               0.4<br>
environs                  9.5.0<br>
et-xmlfile                1.1.0<br>
executing                 1.0.0<br>
frozenlist                1.2.0<br>
future                    0.18.2<br>
gevent                    21.12.0<br>
gevent-websocket          0.10.1<br>
greenlet                  1.1.3<br>
h11                       0.13.0<br>
html5lib                  1.1<br>
icmplib                   3.0.3<br>
idna                      3.3<br>
importlib-metadata        4.11.3<br>
ipykernel                 6.15.2<br>
ipython                   8.4.0<br>
jedi                      0.18.1<br>
jupyter_client            7.3.5<br>
jupyter-core              4.11.1<br>
keyboard                  0.13.5<br>
lxml                      4.8.0<br>
marshmallow               3.18.0<br>
matplotlib-inline         0.1.6<br>
module-wrapper            0.3.1<br>
MouseInfo                 0.1.3<br>
multidict                 5.2.0<br>
nest-asyncio              1.5.5<br>
numpy                     1.22.3<br>
openai                    0.23.0<br>
openpyxl                  3.0.10<br>
outcome                   1.1.0<br>
packaging                 21.3<br>
pandas                    1.4.4<br>
pandas-stubs              1.4.4.220912<br>
parso                     0.8.3<br>
pefile                    2022.5.30<br>
pickleshare               0.7.5<br>
Pillow                    9.0.0<br>
pip                       22.2.2<br>
prompt-toolkit            3.0.30<br>
psutil                    5.9.1<br>
pure-eval                 0.2.2<br>
pyaes                     1.6.1<br>
PyAutoGUI                 0.9.52<br>
pycodestyle               2.8.0<br>
pycparser                 2.21<br>
pyee                      8.2.2<br>
pygame                    2.1.2<br>
PyGetWindow               0.0.9<br>
pyglet                    2.0.dev13<br>
Pygments                  2.13.0<br>
pyinstaller               5.3<br>
pyinstaller-hooks-contrib 2022.10<br>
PyMsgBox                  1.0.7<br>
pymunk                    6.2.1<br>
pyOpenSSL                 21.0.0<br>
pyparsing                 3.0.9<br>
pyperclip                 1.8.2<br>
pyppeteer                 1.0.2<br>
PyQt6                     6.2.2<br>
PyQt6-Qt6                 6.2.2<br>
PyQt6-sip                 13.2.0<br>
PyRect                    0.1.4<br>
Pyrogram                  2.0.57<br>
pyroxy                    0.1<br>
PyScreeze                 0.1.26<br>
PySocks                   1.7.1<br>
python-dateutil           2.8.2<br>
python-dotenv             0.21.0<br>
pytiled-parser            2.0.1<br>
pytweening                1.0.4<br>
pytz                      2021.3<br>
pywin32                   304<br>
pywin32-ctypes            0.2.0<br>
pyzmq                     23.2.1<br>
requests                  2.27.1<br>
scapy                     2.4.5<br>
selenium                  4.1.0<br>
setuptools                63.2.0<br>
shodan                    1.27.0<br>
six                       1.16.0<br>
sniffio                   1.2.0<br>
socks                     0<br>
sortedcontainers          2.4.0<br>
soupsieve                 2.3.1<br>
sqlparse                  0.4.2<br>
stack-data                0.5.0<br>
stdlib-list               0.8.0<br>
TgCrypto                  1.2.3<br>
toml                      0.10.2<br>
tornado                   6.2<br>
tqdm                      4.64.0<br>
traitlets                 5.3.0<br>
trio                      0.19.0<br>
trio-websocket            0.9.2<br>
types-pytz                2022.2.1.0<br>
typing-extensions         3.10.0.2<br>
tzdata                    2022.1<br>
urllib3                   1.26.8<br>
wcwidth                   0.2.5<br>
webdriver-manager         3.8.3<br>
webencodings              0.5.1<br>
websockets                10.3<br>
whichcraft                0.6.1<br>
wsproto                   1.0.0<br>
XlsxWriter                3.0.3<br>
yarl                      1.7.2<br>
zipp                      3.8.0<br>
zope.event                4.5.0<br>
zope.interface            5.4.0<br>
```
</details>

---

3. Будь-яку сторонню бібліотеку встановив на комп'ютер за допомогою `pip install` команди та зразу почав її використовувати, наприклад встановив бібліотеку [requests](https://requests.readthedocs.io/en/latest/):
    ```bash
    pip install requests
    python #Зайдіть в пайтон інтерпретатор
    >>> import requests
    >>> r = requests.get('https://google.com')
    >>> r.status_code
    >>> exit()
    ```
1. Вставив у звіт результат виконання команд (скріншот або стрічки що вивів):
   - 200

3. Ознайомився які ще методи є в бібліотеці [requests, та спробував їх використати](https://requests.readthedocs.io/en/latest/user/quickstart/):
   -
```python
import requests as r

res = r.get('https://api.github.com/events')

print(f'''
url \t {res.url}
just res \t {res}
status code \t {res.status_code}
encoding \t {res.encoding}
raw \t {res.raw}
a lot of text \t {res.text}
''')
```
5. Даний спосіб інсталяції робить бібліотеку загальнодоступною для даної системи. Будь-яке оновлення бібліотеки буде застосоване до всіх Python проектів на Вашому комп'ютері;
    ```bash
    pip show requests
    pip install requests==2.1
    pip show requests
    pip uninstall requests
    ```
1. Вказав у звіті результат виконання команд:
   -
## pip show requests

```
Name: requests
Version: 2.27.1
Summary: Python HTTP for Humans.
Home-page: https://requests.readthedocs.io
Author: Kenneth Reitz
Author-email: me@kennethreitz.org
License: Apache 2.0
Location: d:\software\programs\python3\lib\site-packages
Requires: certifi, charset-normalizer, idna, urllib3
Required-by: cfscrape, openai, shodan, webdriver-manager
```

## pip install requests==2.1

```
Collecting requests==2.1
  Downloading requests-2.1.0-py2.py3-none-any.whl (445 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 445.3/445.3 kB 5.2 MB/s eta 0:00:00
Installing collected packages: requests
  Attempting uninstall: requests
    Found existing installation: requests 2.27.1
    Uninstalling requests-2.27.1:
      Successfully uninstalled requests-2.27.1
Successfully installed requests-2.1.0
```

## pip show requests

```
Name: requests
Version: 2.1.0
Summary: Python HTTP for Humans.
Home-page: http://python-requests.org
Author: Kenneth Reitz
Author-email: me@kennethreitz.com
License: Copyright 2013 Kenneth Reitz
Location: d:\software\programs\python3\lib\site-packages
Requires:
Required-by: cfscrape, openai, shodan, webdriver-manager
```

## pip uninstall requests

```
Found existing installation: requests 2.1.0
Uninstalling requests-2.1.0:
  Would remove:
    d:\software\programs\python3\lib\site-packages\requests-2.1.0.dist-info\*
    d:\software\programs\python3\lib\site-packages\requests\*
Proceed (Y/n)? y
  Successfully uninstalled requests-2.1.0
```

---

---

### Робота у віртуальному середовищі 
1. [Віртуальні середовища в Python](https://docs.python.org/3/library/venv.html) - це ізольовані середовища для роботи з 'замороженою' версією Python та його бібліотек. Середовище створюється для кожного проекту окремо і буде мати ті самі характеристики в не залежності де та на якій системі буде запущено;
2. Для створення `VENV` та його активації виконав команди:
    ```bash
    python -m venv ./my_env
    source my_env/Scripts/activate
    pip install requests
    deactivate
    pip show requests
    ```
1. Вказав у звіті що вивела остання команда та чому?
   -
```
Name: requests
Version: 2.28.1
Summary: Python HTTP for Humans.
Home-page: https://requests.readthedocs.io
Author: Kenneth Reitz
Author-email: me@kennethreitz.org
License: Apache 2.0
Location: d:\software\programs\python3\lib\site-packages
Requires: certifi, charset-normalizer, idna, urllib3
Required-by: cfscrape, openai, shodan, webdriver-manager
```

---
   - Тому що може. Вона так запрограмованна/написана. В неї не було вибору.

3. Всі створені файли НЕ потрібно комітити в репозиторій. Щоб уникнути такого автоматично створив файл `.gitignore` у кореневій папці та вказав в ньому папки які потрібно ігнорувати.
---

### Робота з Pipenv
1. [Pipenv](https://pipenv.pypa.io/en/latest/) - це інструмент для спрощення інсталяції сторонніх бібліотек та створення віруального середовища для кожного проекту. Для його інсталяції застосував команду:
    ```bash
    pip install pipenv
    # Після успішного виконання команди виконайте
    pipenv --help
    ``` 
1. Вказав у звіті які команди можна виконувати за допомогою `pipenv`:
   -
```
Usage: pipenv [OPTIONS] COMMAND [ARGS]...

Options:
  --where                         Output project home information.
  --venv                          Output virtualenv information.
  --py                            Output Python interpreter information.
  --envs                          Output Environment Variable options.
  --rm                            Remove the virtualenv.
  --bare                          Minimal output.
  --man                           Display manpage.
  --support                       Output diagnostic information for use in
                                  GitHub issues.
  --site-packages / --no-site-packages
                                  Enable site-packages for the virtualenv.
                                  [env var: PIPENV_SITE_PACKAGES]
  --python TEXT                   Specify which version of Python virtualenv
                                  should use.
  --three                         Use Python 3 when creating virtualenv.
                                  Deprecated
  --clear                         Clears caches (pipenv, pip).  [env var:
                                  PIPENV_CLEAR]
  -q, --quiet                     Quiet mode.
  -v, --verbose                   Verbose mode.
  --pypi-mirror TEXT              Specify a PyPI mirror.
  --version                       Show the version and exit.
  -h, --help                      Show this message and exit.


Usage Examples:
   Create a new project using Python 3.7, specifically:
   $ pipenv --python 3.7

   Remove project virtualenv (inferred from current directory):
   $ pipenv --rm

   Install all dependencies for a project (including dev):
   $ pipenv install --dev

   Create a lockfile containing pre-releases:
   $ pipenv lock --pre

   Show a graph of your installed dependencies:
   $ pipenv graph

   Check your installed dependencies for security vulnerabilities:
   $ pipenv check

   Install a local setup.py into your virtual environment/Pipfile:
   $ pipenv install -e .

   Use a lower-level pip command:
   $ pipenv run pip freeze

Commands:
  check         Checks for PyUp Safety security vulnerabilities and against
                PEP 508 markers provided in Pipfile.
  clean         Uninstalls all packages not specified in Pipfile.lock.
  graph         Displays currently-installed dependency graph information.
  install       Installs provided packages and adds them to Pipfile, or (if no
                packages are given), installs all packages from Pipfile.
  lock          Generates Pipfile.lock.
  open          View a given module in your editor.
  requirements  Generate a requirements.txt from Pipfile.lock.
  run           Spawns a command installed into the virtualenv.
  scripts       Lists scripts in current environment config.
  shell         Spawns a shell within the virtualenv.
  sync          Installs all packages specified in Pipfile.lock.
  uninstall     Uninstalls a provided package and removes it from Pipfile.
  update        Runs lock, then sync.
  verify        Verify the hash in Pipfile.lock is up-to-date.
```

3. Для створення нового середовища та інсталяції бібліотек виконав наступні команди:
    ```bash
    pipenv --python 3.10
    pipenv --venv
    pipenv run python -V
    pipenv install requests
    ```
1. Переконався що у мене створились файли `Pipfile` та `Pipfile.lock`. Що в них знаходиться?
   - html

3. Створив пайтон файл та записав в нього наступну програму:
    ```python
    import requests

    response = requests.get('https://httpbin.org/')
    for line in response.iter_lines():
        print(line)
    ```
1. Спробував запустити програму з Visual Studio. Запустив програму з командної стрічки. Запустив програму зайшовши у віртуальне середовище за допомогою команди `pipenv shell`. Результати записав у звіт:
   - Родился 'Pipfile', зміна зовнішнього вигляд консолі.

3. Вибрав якусь бібліотеку на [Pypi](https://pypi.org/) та спробував її інсталювати. Знайшов документацію цієї бібліотека та спробував виконати якісь приклади.
5. Visual Studio дозволяє змінити Python інтерпретатор для запуску через кнопку `Run` (трикутник з трьома кутами). Для цього викликав командну палітру з меню `View -> Command Palette...` та в ній набрав `Python: Select interpreter`. Якщо у Вас вже є інстальоване віртуальне середовище, Visual Studio відобразить всі доступні інтерпретатори.
6. Змінив інтерпретатор Python із Вашого середовища та виконав скрипт через кнопку `Run`. Представив результат у звіті:
   -
```
Python 3.10.6 64-bit
```
---

### Робота зі змінними середовища
1. Середовища також можна параметризувати за допомогою змінних середовища (*Environment Variables*). Для цього у папці повинен буди файл `.env` із заданими змінними у форматі `KEY=VALUE`. Pipenv автоматично розпізнає ці файли та робить їх доступними всередині середовища. Створив файл `.env` та виконав наступний код:
```python
import os
os.environ['HELLO']
```
1. Що буде якщо виконати скрипт без активації віртуального середовища?
  > Буде ерор, кей ерор, який хеллоу.
---

### **Висновок**: 
> Під час виконання лабораторної роботи я досягнув мети роботи, а саме проробив роботу у віртуальних середовищах. 

> У висновку відповів на запитання:
- Що зроблено в роботі?
  > В роботі була пророблена робота у віртуальних середовищах і тим що було з ним повязано, перерахувати я манав вже і так приближаємось до 500 рядку.
- Чи досягнуто мети роботи?
  > Так, мета робити була досягнута в процесі її виконання.
- Які нові знання отримано?
  > Які було пророблені під час виконання лабораторної роботи ті і отримав.
- Чи вдалось відповісти на всі питання задані в ході роботи?
  > Вроді як. 
- Чи вдалося виконати всі завдання?
  > Так, всі завдання було виконано під час виконання роботи по пробленню роботи у віртуальних середовищах.
- Чи виникли складності у виконанні завдання?
  > Поки ні. Погано старались.
- Чи подобається такий формат здачі роботи (Feedback)?
  > Цілком і повністью.
- Побажання для покращення (Suggestions)?
  > Я б зменшив кількість смайликів приблизно до 0.
---
