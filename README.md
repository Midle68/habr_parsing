# Проект "Анализ постов на habr.com"

В рамках данного проекта необходимо осуществить парсинг данных с веб-сайта. В качества веб-сайта взят habr.com. Необходимо осуществить парсинг лучших постов за все время. Данные для парсинга: 1) параметры - наименование статьи, дата загрузки, категория, к которой пост относится; количество голосов и 2) целевой показатель - число просмотров. 

Параметр 'количество голосов' можно также использовать как целевой показатель, поэтому и информация по нему была собрана. Более того, рейтинг постов определяется именно количеством голосов, а не просмотров. Однако в качестве независимого параметра 'количество голосов' не подходит, поскольку может сильно зависеть от количества просмотров. 

В дальнейшем можно рассмотреть не только лучшие за все время посты, но и увеличить выборку еще б**о**льшим объемом повседневных постов.

Объем выборки составил 997 статей (для 3 не было обнаружено количество просмотров, поэтому от них решено было избавиться. В дополнение, результат работы парсера (база данных) был сохранен в отдельный файл 'posts_data.csv')

## План проекта:
1. [Импортирование библиотек](#import)
2. [Парсинг данных](#parsing)
3. [Предобработка данных и Feature Engineering](#preprocessing)
    - [Типы данных](#dtypes)
    - [Проверка на аномальные значения](#anomalies)
    - [Feature Engineering](#feature_engineering)
4. [Исследовательский анализ данных](#eda)
    - [Количество постов по годам](#posts_per_year)
    - [Количество постов по категориям](#posts_categories)
    - [Категории постов по годам публикаций](#categories_per_year)
    - [Количество просмотров по дате](#views_per_date)
        - [Количество просмотров по году публикации](#views_per_year)
        - [Количество просмотров по месяцам](#views_per_month)
        - [Количество просмотров по дням](#views_per_day)
        - [Количество просмотров по часам](#views_per_hour)
        - [Количество просмотров по минутам](#views_per_minute)
    - [Количество просмотров по категориям](#views_per_category)
    - [Самые популярные слова в названиях постов](#popular_words)
        - [По частоте упоминаний](#words_per_frequency)
        - [По обществу количеству просмотров](#words_per_views)
        - [По количеству голосов](#words_per_votes)
    - [Количество просмотров по длине названия](#views_to_length)
    - [Корреляция между параметрами](#correlation)

## Используемые библиотеки:

`matplotlib`, `nltk`, `numpy`, `pandas`, `pymystem3`, `re`, `seaborn`, `selenium`, `time`

## Статус проекта

В процессе разработки.
