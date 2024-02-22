# E-learning_project
A/B-testing, SQL, ETL, API-function

Стек: Python(pandas, pandahouse, numpy, seaborn, matplotlib, scipy, urllib, requests), Redash

# Входные данные
В качестве входных данных имеете 4 csv-файла:

groups.csv - файл с информацией о принадлежности пользователя к контрольной или экспериментальной группе (А – контроль, B – целевая группа) 

groups_add.csv - дополнительный файл с пользователями, который прислали спустя 2 дня после передачи данных

active_studs.csv - файл с информацией о пользователях, которые зашли на платформу в дни проведения эксперимента

checks.csv - файл с информацией об оплатах пользователей в дни проведения эксперимента

# Цели
1) Проанализировать итоги A/B–тестирования и сделать вывод, стоит ли запускать новую механику оплаты на всех пользователей.
2) Написать 2 SQL запроса: а) выгрузить информацию о количестве студентов, которые правильно решили 20 задач за текущий месяц;
                           б) в одном запросе выгрузить следующую информацию о группах пользователей: ARPU, ARPAU, CR в покупку, СR активного пользователя в покупку, CR пользователя из                                   активности по математике в покупку курса по математике.
3) Написать 2 функции: а) автоматически подгружать информацию из дополнительного файла groups_add.csv и на основании дополнительных параметров пересчитывать метрики;
                       б) строить графики по получаемым метрикам.

# Итоги
1) Для задачи 1 были подсчитаны средний чек, CR и ARPU; применен тест Шапиро-Уилка для проверки на нормальность, проверено различие в дисперсиях через критерий Левена, также применены Т-тест и Хи-квадрат.
2) Вторая задача была написана в ClickHouse и выгружена в pandas через ETL.
3) В третьей задаче использовался API.
