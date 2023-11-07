# Парсер сайтов

## Описание
#### Парсер сайтов https://docs.python.org/  и https://peps.python.org/. 

Собирает ссылки на статьи о нововведениях в Python, переходит по ним и забирает информацию об авторах и редакторах статей. Собирает информацию о статусах версий Python. Скачивает архив с актуальной документацией. Собирает данные обо всех докментах PEP, подсчитывает количество PEP в каждом статусе и общее количество PEP.

###  Установка и настройки
  * Шаг первый: клонируем репозиторий
```python
git clone git@github.com:Nurbek878/bs4_parser_pep.git
```
 * Переходим в папку с проектом 
```sh 
cd bs4_parser_pep
``` 
* Создаем и активируем виртуальное окружение 
```sh 
python -m venv venv 
source venv/bin/activate 
``` 
* Обновляем менеджер пакетов pip
```sh 
pip install --upgrade pip 
``` 
* Устанавливаем необходимые зависимости 
```sh 
pip install -r requirements.txt
``` 
 * Переходим в папку src/ 
```sh 
cd src/
``` 
### Выбираем режим работы парсера:
*  ```python main.py whats-new``` - статьи по версиям Python (https://docs.python.org/3/whatsnew).
*  ```python main.py latest-versions``` - статусы последних версий  (https://docs.python.org/3/).
*  ```python main.py download``` - загрузка файла документации по последней версии Python (https://docs.python.org/3/download.html).
*  ```python main.py pep``` - формирование таблицы со статусами PEP (https://peps.python.org/).

### Выбираем опциональные аргументы :
```
optional arguments:
  -h, --help            show this help message and exit
  -c, --clear-cache     Очистка кеша
  -o {pretty,file}, --output {pretty,file}
                        Дополнительные способы вывода данных
```
Например, для того чтобы запустить парсер в режиме PEP с очистко кеша и с выводом в файл, вводим команду:
```sh 
python main.py pep -c --output file
``` 

### Стек
-   [Python](https://www.python.org/)
-   [BeautifulSoup](https://pypi.org/project/beautifulsoup4/)
-   [lxml](https://pypi.org/project/lxml/)
-   [PrettyTable](https://pypi.org/project/prettytable/)
-   [requests-cache](https://pypi.org/project/requests-cache/)
-   [tqdm](https://pypi.org/project/tqdm/)


##### Автор

- [@nurbek878](https://github.com/Nurbek878)