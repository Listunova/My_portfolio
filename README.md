# *__Портфолио: аналитик данных__*
## *__Обо мне__*
#### Привет! Меня зовут Аня, я начинающий аналитик данных. Также я обучаюсь на магистратуре "Российского государственного университета нефти и газа им.Губкина" по профилю "Автоматизированные системы обработки информации и управления" направления "Информатика и вычислительная техника". В этом репозитории вы можете найти некоторые из моих проектов, выполненных во время обучения и практики.
## *__Навыки и технологии__*
#### -Инструменты анализа данных: SQL, Excel
#### -Языки программирования и библиотеки: Python, Pandas, math
#### -Системы управления базами данных: MySQL,PostgreSQL
#### -Средства визуализации данных:  PowerBi, Matplotlib, seaborn
#### -Инструменты для машинного обучения: TensorFlow
## *__Проекты__*
#### *__Проект 1: Калькулятор юнит-экономики онлайн-школы в Excel__*
[Проект](<https://docs.google.com/spreadsheets/d/1mQ56qskyZg6YuYIOChsoX7wkBgosbT-K/edit#gid=1670325505>)
#### Что нужно было сделать:
#### *Задача №1.* Настроить в калькуляторе учет корректировок планов маркетинга
#### *Задача №2.* Пересчитать план найма преподавателей
#### *Как решала:* в первом задании добавила в список параметров нашего калькулятора показатель "Поправочный коэф-т на привлечение", настроила динамический расчёт количества новых студентов за период 05.21-04.22 с поправкой на этот коэффициент. Если для 05.21-04.22 он был равен 120%, то в каждый месяц этого периода рассчётное значение количества новых студентов должно быть больше на 20%. Во втором задании добавила в калькулятор Найма преподавателей возможность изменять входных параметры: Пропускную способность П и Retention П - с помощью дополнительного столбца с процентными изменениями, просчитала сценарий, при котором Пропускная способность П увеличится на 15 процентов, а Retention П упал на 2 процента.
#### *В результате* была посчитана юнит-экономика продукта и представлен сценарий по настройке параметров для выхода на 25-ти процентную маржинальность. Также были визуализированы пользователи, где и в каком объеме смотрят фильмы на платформе. 
#### *__Проект 2: Моделирование изменения балансов студентов в SQL__*
[Проект](<https://docs.google.com/spreadsheets/d/18hvQglPqxNenlaqilQr1HSVvQ1915FlA/edit?usp=sharing&ouid=110581665585668535971&rtpof=true&sd=true>)
#### Что нужно было сделать:
#### *Задача №1.* Посмотеть на изменения балансов студентов (на примере топ-1000 строк), собранных из CTE. 
#### *Задача №2.* Создать визуализацию (линейную диаграмму) итогового результата. 
#### *Как решала:* узнала, когда была первая транзакция для каждого студента. Начиная с этой даты, я собирала баланс уроков. Собрала таблицу с датами за каждый календарный день 2016 года. Нашла все изменения балансов, связанные с успешными транзакциями. Выбрала все транзакции из таблицы payments, сгруппировала их по user_id и дате транзакции (без времени) и посчитала сумму по полю classes. Нашла баланс студентов, который сформирован только транзакциями. Нашла изменения балансов из-за прохождения уроков. Создала CTE для хранения кумулятивной суммы количества пройденных уроков. Создала CTE balances с вычисленными балансами каждого студента.В итоге посмотрела, как менялось общее количество уроков на балансах студентов.
#### *В результате* получила запрос, который собирает данные о балансах студентов за каждый прожитый ими день.
#### *__Проект 3: Эксперимент и калькулятор. Анализ АБ-Теста*
[Проект](<https://drive.google.com/file/d/1UGDSIF0AvP9xJhG80iQp3pL-IT-QkFjF/view?usp=sharing>)

[Проект в   Excel](<https://docs.google.com/spreadsheets/d/1Tdusblrrz0PofjYjrje3f3aIQZZ_VXyk/edit?usp=sharing&ouid=110581665585668535971&rtpof=true&sd=true>)
#### Что нужно было сделать:
#### *Задача:* Необходимо проанализировать и визуализировать результаты, провести сегментацию, а также сделать выводы и сформулировать рекомендации для дальнейших запусков АБ Теста.
#### *Как решала: Импортировала данные в окружение *Jupyter Notebook*, исключа из таблиц все строки, в которых есть нулловые значения и построила группировку по количеству в каждом городе и визуализировала с помощью гистограммы. Далее построила агрегацию таблицы с платежами, где вычислила сумму платежей на каждого клиента и соединила таблицу с клиентской таблицей, также подтянула к каждой торговой точке город, в котором она находится. Создала функцию ***test_calc***, которая будет вычислять значение t-критерия (критерия Стьюдента) и *p_value* для сравнения средних и с помощью функции *print* выводить сообщение о том, существует ли разница между средними (на основании *p_value*).Также создала функцию ***mann_whitney_func***, которая будет рассчитывать значение критерия Манна Уитни и p_value для сравнения распределений и с помощью функции *print* выводить сообщение о том, существует ли разница между средними (на основании *p_value*).Отбросила все торговые точки, в которых не было заплачено ни одного рубля ни одним клиентом или в которых пустует или контрольная, или тестовая группа. Применила функцию ***test_calc*** и ***mann_whitney_func*** Сделала сегментацию результатов АБ Теста по городам. Сделала отчет по АБ Тесту и выгрузила полученные результаты в Excel.
#### *В результате* Построена таблица, которая в удобной форме хранит результаты АБ Теста. 
