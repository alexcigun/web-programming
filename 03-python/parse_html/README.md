BeautifulSoup
=============

**Задача.** Дана главная страница Хабра, выдрать все заголовки постов.

**Решение**. Используем библиотеку [BeautifulSoup](http://www.crummy.com/software/BeautifulSoup/bs4/doc/),
которая предоставлять способы удобной работы с html. Это почти что jQuery из мира Питона.

    $ python script.py 
    Яндекс.Кит: новая прошивка для смартфонов
    Теплый ламповый звук
    10 анти-паттернов навигации в Android
    Новый интерфейс Яндекс.Метро и технологии, с помощью которых он работает
    TCP/IP по аудиоканалу
    Вася говорит
    Одно кольцо, чтоб править всеми… устройствами
    Реакция разных компаний на уязвимости их ресурсов
    Исследуем обфускацию прошивки Linksys WRT120N
    10 миллионов игроков в Pokemon

Задание
-------

Вашей программе подаётся главная страница Хабра. Перегоните данные из html-страницы в csv-таблицу из пяти колонок:
название статьи, автор поста, дата создания, первая строчка поста, список хабов. Также сохраните эти данные в файле
data.json в формате [JSON](http://json.org/) в кодировке utf-8 так:

    [
        {
            'title': 'Опасное развлечение: простой для повторения генератор высокого напряжения',
            'author': 'kreosan',
            'data': '20.02.2014, 18:27',
            'first_line': 'Добрый день, уважаемые хабровчане.',
            'hubs': [
                'Электроника для начинающих', 'DIY или Сделай Сам'
            ]
        },
        {
            ...
        }
    ]

Форматирование в json можно не соблюдать.