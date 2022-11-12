# Звіт до роботи Lab4

## Тема: Віртуальні середовища

### Мета: Оволодіти основам роботи з сторонніми бібліотеками

---

### Виконання роботи:

### Основи роботи з сторонніми бібліотеками

- Я ввів команду `pip list`, щоб вивести список встановлених бібліотек:

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
certifi                   2021.10.8<br>
cffi                      1.15.0<br>
cfscrape                  2.1.1<br>
charset-normalizer        2.0.7<br>
environs                  9.5.0<br>
et-xmlfile                1.1.0<br>
executing                 1.0.0<br>
frozenlist                1.2.0<br>
future                    0.18.2<br>
PyMsgBox                  1.0.7<br>
pymunk                    6.2.1<br>
pyOpenSSL                 21.0.0<br>
pyparsing                 3.0.9<br>
pyperclip                 1.8.2<br>
pyppeteer                 1.0.2<br>
PyQt6                     6.2.2<br>
pyzmq                     23.2.1<br>
requests                  2.27.1<br>
scapy                     2.4.5<br>
selenium                  4.1.0<br>
setuptools                63.2.0<br>
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

- Я вставив код з прикладу у файл `.ipynb`

```py
import requests

res = requests.get('https://google.com')
print(res.status_code)
```

у відповідь я получив код 200

```txt
200
```

- Поекспериментував з різнимим методами рекюестс:

```py
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

```<br>
url  -   https://api.github.com/events<br>
just res    -    Response [200]<br>
status   -   code 200<br>
encoding   -     utf-8<br>
raw     -    urllib3.response.HTTPResponse object at 0x000001B1E2B52890<br>
a lot of text    -   [{"id":"24554816296","type":"PushEvent","actor":{"id":28802726,"login":"lapnguyen12b","display_login":"lapnguyen12b","gravatar_id":"","url":"https://api.github.com/users/lapnguyen12b","avatar_url":"https://avatars.githubusercontent.com/u/28802726?"},"repo":{"id":550319158,"name":"lapnguyen12b/Solidity-tutorial","url":"https://api.github.com/repos/lapnguyen12b/Solidity-tutorial"},"payload":{"push_id":11306606032,"size":2,"distinct_size":1,"ref":"refs/heads/master","head":"d6adc79cd41c0800c77a7c5c615a2804a6f5edd1","before":"7d0dfeaac16bfb43091c120953568284ab62edfb","commits":[{"sha":"b8b15243e4febea83269cb958dc059d58354e491","author":{"email":"lapnguyen12b@gmail.com","name":"lapnv"},"message":"first constract","distinct":false,"url":"https://api.github.com/repos/lapnguyen12b/Solidity-tutorial/commits/b8b15243e4febea83269cb958dc059d58354e491"},{"sha":"d6adc79cd41c0800c77a7c5c615a2804a6f5edd1","author":{"email":"lapnguyen12b@gmail.com","name":"lnv1995"},"message":"Merge pull request #1 from lapnguyen12b/lapnv/first-constract\n\nFirst constract","distinct":true,"url":"https://api.github.com/repos/lapnguyen12b/Solidity-tutorial/commits/d6adc79cd41c0800c77a7c5c615a2804a6f5edd1"}]
```
</details>

---

- Я ввів наступні команди:

```
pip show requests
pip install requests==2.1
pip show requests
pip uninstall requests
```

І ось що вони вивели у консольку:

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
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 445.3/445.3 kB 3.1 MB/s eta 0:00:00
Installing collected packages: requests
  Attempting uninstall: requests
    Found existing installation: requests 2.27.1
    Uninstalling requests-2.27.1:
      Successfully uninstalled requests-2.27.1
Successfully installed requests-2.1.0
```

## pip show requests

видно що інсталювалась старіша версія бібліотеки

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

### Робота у віртуальному середовищі

- Я ввів по черзі запропоновані команди, але деякі з них видавали помилку

```py
python - m venv ./my_env
source my_env/Scripts/activate
pip install requests
deactivate
pip show requests
```

- Команда `pip show requests` вивела опис бібліотеки

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

### Робота з Pipenv

- Я інсталював піпенв бібліотеку, та написав `pipenv --help`. Ось що вивелось:

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

- Я ввів код з прикладу і запустив з терміналу VS Code. У відповідь я отримав код сторінки

```text
b'<!DOCTYPE html>'
b'<html lang="en">'
b''
b'<head>'
b'    <meta charset="UTF-8">'
b'    <title>httpbin.org</title>'
b'    <link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700|Source+Code+Pro:300,600|Titillium+Web:400,600,700"'
b'        rel="stylesheet">'
b'    <link rel="stylesheet" type="text/css" href="/flasgger_static/swagger-ui.css">'
b'    <link rel="icon" type="image/png" href="/static/favicon.ico" sizes="64x64 32x32 16x16" />'
b'    <style>'
b'        html {'
b'            box-sizing: border-box;'
b'            overflow: -moz-scrollbars-vertical;'
b'            overflow-y: scroll;'
b'        }'
b''
b'        *,'
b'        *:before,'
b'        *:after {'
b'            box-sizing: inherit;'
b'        }'
b''
b'        body {'
b'            margin: 0;'
b'            background: #fafafa;'
b'        }'
b'    </style>'
b'</head>'
b''
```

### Робота зі змінними середовища

- Я створив файл `.env` та запистик код з пикладу, мені вивело таку помилку:

```
KeyError: 'HELLO'
```
### Висновок
- Що зроблено в роботі - Навилився працювати з віртуальними середовищами.
- Чи досягнуто мети роботи - так;
- Які нові знання отримано - знання з ООП;
- Чи вдалось відповісти на всі питання задані в ході роботи - ні;
- Чи вдалося виконати всі завдання;
- Чи виникли складності у виконанні завдання - так;
- Чи подобається такий формат здачі роботи (Feedback)- так;
- Побажання для покращення (Suggestions) - ;