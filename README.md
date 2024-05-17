Задания данной практики:

                                                                    Практика5.
1. В таблице stars.csv содержится информация о 240 звёзд.
Temperature (K) – температура в Кельвинах.
Luminosity (L/Lo) – cветимость звезды относительно солнечной светимости.
Radius (R/Ro) – радиус звезды по отношению к радиусу солнца
Absolute magnitude (Mv) – абсолютная звёздная величина
Star color – цвет звезды
Star type – тип звезды, число от 0 до 5, где
0 — Red Dwarf,
1 — Brown Dwarf,
2 — White Dwarf,
3 — Main Sequence,
4 — Super Giants,
5 — Hyper Giants;
Spectral Class – спектральный класс звезды (один из O, B, A, F, G, K и M).
Задание:
1. обработать значения в столбце с цветом: привести значения в этом столбце к общему виду (в частности, значения ‘Blue white’, ‘Blue White’ и ‘Blue-white’ должны совпадать);
2. добавить столбец, в котором тип звезды указан полной строкой, а не числом;
3. для столбца со спектральным классом, наоборот, добавить столбец с числами, в следующем соответствии:
O → 0,
B → 1,
A → 2,
F → 3,
G → 4,
K → 5,
M → 6;
4. посчитать количество звезд каждого цвета, каждого типа и каждого спектрального класса;
5. среди звезд каждого типа найти минимальные, средние и максимальные значения абсолютной звездной величины;
6. среди звезд каждого класса найти минимальные, средние и максимальные значения температуры;
7. вычислить попарные корреляции между всеми числовыми столбцами.


DataFrame.corr() – метод вычисляет попарную корреляцию столбцов, исключая значения NA/null. Он возвращает матрицу корреляции DataFrame.
DataFrame.corr(method='pearson', min_periods=1)
– method {'pearson', 'kendall', 'spearman'} или вызываемый
Метод корреляции:
Пирсон: стандартный коэффициент корреляции
Кендалл: коэффициент корреляции Тау Кендалла
копьеносец: ранговая корреляция Спирмена
– min_periods: целое число, необязательно. Минимальное количество наблюдений, необходимых для пары столбцов, чтобы получить действительный результат.


 
2. В таблице sunspot.csv содержит данные о наблюдениях солнечных пятен с 1818 года.
year — год наблюдения;
month — месяц наблюдения;
day — день наблюдения;
Number of spots — суммарное количество солнечных пятен, замеченных в этот день. В столбце приводится среднее значение, если есть данные о наблюдениях от разных обсерваторий. Если данных за этот день нет, то в столбце ставится значение -1;
Standard Deviation — среднеквадратическое отклонение наблюдений с разных станций; Если данных за этот день нет, то в столбце ставится значение -1;
Observations — количество станций, доложивших наблюдения за этот день;

                                                                            Практика6.
Задача про Титаник
1.  Обработать значения в столбцах:
– Age. При отсутствии данных задать полям значение равное медиане по возрасту из всей выборки.
– Embarked. При отсутствии данных присвоить пассажирам порт, в котором село больше всего людей.
– Fare. При отсутствии данных заменить цену медианой по цене из всей выборки.
2. Перевести категории в числовое представление. Age , embarked
3. Вывести статистику выживаемости в зависимости от:
– класса;
– пола;
– возраст;
– наличие семьи на борту.
Информацию представить в числовом и графическом виде.
4. Посчитать сводку (описательная статистика) по всем числовым полям выборки – отдельно по мужчинам и по женщинам.
5. Подсчитать количество:

                                                                              Практическое занятие 7
                                                                                Библиотека Pandas

Дополнительная информация
https://pandas.pydata.org/pandas-docs/stable/reference/index.html

В таблице NBA.csv находятся физиологические данные 4550 баскетболистов NBA, собранные в период с 1947 по 2017.
– Player Full Name – имя баскетболиста;
– Birth Date – дата рождения;
– Year Start – год начала карьеры;
– Year End – год завершения карьеры;
– Position – позиция игрока:
F – нападающий;
G – защитник;
C – центровой;
G-F – на протяжении карьеры выступал и на позиции защитника и на позиции нападающего;
F-C – на протяжении карьеры выступал и на позиции нападающего и на позиции центрового;
– Height – рост в сантиметрах;
– Wingspan – размах рук в сантиметрах;
– Weight – вес в фунтах (0.45359237 кг);

Задание:
1. перевести вес в килограммы;
2. найти самого высокого и самого низкого игрока;

DataFrame.idxmax([ось, пропуск, numeric_only])	Возвращает индекс первого появления максимума на запрошенной оси.
DataFrame.idxmin([ось, пропуск, numeric_only])
Возвращает индекс первого появления минимума на запрошенной оси.
DataFrame.loc
Доступ к группе строк и столбцов по меткам или логическому массиву.

3. найти самого легкого и тяжелого игрока;
4. найти игроков с самым маленьким и самым большим размахом рук;
5. найти корреляции между столбцами с ростом, весом и размахом рук; построить диаграмму рассеяния (scatter plot) для этих показателей (опционально, если знакомы с линейной регрессией и инструментами для её вычисления в python, можно добавить график линейной регрессии);

DataFrame.corr([метод, мин_периоды, ...])
Вычислите попарную корреляцию столбцов, исключая значения NA/null.
numpy.polyfit(x, y, deg, rcond=None, full=False, w=None, cov=False)	Вычисление коэффициентов линейной регрессии

6. добавить столбец с продолжительностью карьеры;

DataFrame.apply(функ[, ось, необработанный, ...])
Примените функцию вдоль оси DataFrame.

7. добавить столбец с индексом массы тела;
8. исследовать, как зависят средняя продолжительность карьеры, средний рост, средний вес и средний размах рук в зависимости от позиции (построить графики);

DataFrame.groupby([по, оси, уровню, ...])
Группируйте DataFrame с помощью преобразователя или серии столбцов.
DataFrame.mean([ось, пропуск, numeric_only])	Возвращает среднее значение значений по запрошенной оси.

9. исследовать, как меняются те же самые показатели с течением времени (построить графики);

– братьев и сестер на борту (SibSp);
– родителей и детей на борту (Parch).
7. Определить распределение по классам кают:
– женщин;
– мужчин.
Информацию представить в числовом и графическом виде.

                                                                                Практическое занятие 8
                                                                                  Библиотека Pandas

Исследовательская группа GroupLens Research предлагает несколько наборов данных о рейтингах фильмов, проставленных пользователями сайта MovieLens в конце 1990-х – начале2000-х годов. Наборы содержат рейтинги фильмов, метаданные о фильмах (жанр и год выхода) и демографические данные о пользователях (возраст,почтовый индекс, пол и род занятий).
Набор MovieLens 1M содержит 1 000 000 рейтингов 4000 фильмов, проставленных 6000 пользователей. Данные распределены по трем таблицам: рейтинги, информация о пользователях и информация о фильмах.
Задание:
1. Вычислить средние рейтинги для конкретного фильма в разрезе пола и возраста.
2. Получить средние рейтинги каждого фильма по группам зрителей одного пола, используя метод pivot_table.
3. Найти фильмы, по которым мужчины и женщины сильнее всего разошлись в оценках. (Можно добавить столбец, содержащий разность средних, а затем отсортировать по нему.)
4. Найти фильмы, вызвавшие наибольшее разногласие у зрителей независимо от пола. (Разногласие можно изменить с помощью дисперсии или стандартного отклонения оценок.)


                                                                                Практическое занятие 9
                                                                                  Библиотека Pandas
Исторические цены на акции Alphabet Inc. (GOOG)
Период времени: 1 апреля 2020 г. – 1 октября 2020 г.
Описание набора данных:
– Date: указывает дату, на которую даны подробные сведения об акциях.
– Open: показывает цену открытия акции на эту дату.
– High: показывает самую высокую цену, до которой акция поднялась в этот день.
– Low: показывает самую высокую цену, до которой упала акция в этот день.
– Close: показывает цену закрытия акции на эту дату.
– Volume: показывает количество акций, проданных на эту дату.
– Adj Close: Скорректированная цена закрытия — это цена закрытия акции в любой день торгов, в которую были внесены поправки, включающие любые распределения и корпоративные действия, которые произошли в любое время до открытия следующего дня.

Задание:
1. Напишите программу Pandas для создания линейного графика исторических цен на акции Alphabet Inc. между двумя конкретными датами.
2. Напишите программу Pandas для создания линейного графика цен открытия и закрытия акций Alphabet Inc. между двумя конкретными датами.
3. Напишите программу Pandas для создания гистограммы объема торгов акциями Alphabet Inc. между двумя конкретными датами.
4. Напишите программу Pandas для создания гистограммы цен открытия и закрытия акций Alphabet Inc. между двумя конкретными датами.
5. Напишите программу Pandas для создания гистограммы цен открытия и закрытия акций Alphabet Inc. между двумя конкретными датами.
6. Напишите программу Pandas для создания гистограмм открытия, закрытия, высоких и низких цен на акции Alphabet Inc. между двумя конкретными датами. 
7. Напишите программу Pandas для построения горизонтальной и кумулятивной гистограммы цен открытия акций Alphabet Inc. между двумя конкретными датами.

  
                                                                                                  Практическое занятие 10
                                                                                                  Визуализация данных
В этом наборе данных у нас есть исторические данные о населении для каждой страны/территории мира по различным параметрам, таким как размер территории страны/территории, название континента, название столицы, плотность, темпы роста населения, рейтинг на основе численности населения, Процент мирового населения и т. д.
Глоссарий набора данных (по столбцам)
Rank: Рейтинг по численности населения.
CCA: 3-значный код страны/территории.
Country/Territories: название страны/территорий.
Capital: Название столицы.
Continent: Название континента.
2022 Population: Численность населения страны/территорий в 2022 году.
2020 Population: Численность населения страны/территорий в 2020 году.
2015 Population: Численность населения страны/территорий в 2015 году.
2010 Population: Численность населения страны/территорий в 2010 году.
2000 Population: Население страны/территорий в 2000 году.
1990 Population: Население страны/территорий в 1990 году.
1980 Population: Население страны/территорий в 1980 году.
1970 Population: Население страны/территорий в 1970 году.
Area (km²): Размер площади страны/территорий в квадратных километрах.
Density (per km²): Плотность населения на квадратный километр.
Growth Rate: темпы роста населения по странам/территориям.
World Population Percentage: процент населения по каждой стране/территории.


Задание:
1. Выполнить загрузку данных.
2. Получить представлении о наборе данных с помощью методов shape, head, describe, info библиотеки pandas. Посчитать количество пустых значений в признаках с помощью библиотеки numpy.
3. Произвести разведочный анализ данных по данному набору данных – визуализировать данные с помощью библиотек matplotlib, seaborn.
Построить:
– Парные диаграммы (pairplots)
Функция pairplot() строит сетку элементами, которой являются графики попарного сравнения заданного набора признаков. Для лучшего визуального представления применим стиль ticks.
Пример,
sns.set(style="ticks")
mpg = sns.load_dataset("mpg")
mpg_mod = mpg[["mpg", "horsepower", "displacement", "origin"]]
sns.pairplot(mpg_mod)
 
Рисунок 1 – Диаграмма, построенная с функцией pairplot()

– Тепловую карту по матрице корреляции
Корреляционная тепловая карта – это тепловая карта, которая показывает 2D корреляционную матрицу между двумя дискретными измерениями, используя цветные ячейки для представления данных, обычно в монохроматическом масштабе.
seaborn.heatmap(data, *, vmin=None, vmax=None, cmap=None, center=None, robust=False, annot=None, fmt='.2g', annot_kws=None, linewidths=0, linecolor='white', cbar=True, cbar_kws=None, cbar_ax=None, square=False, xticklabels='auto', yticklabels='auto', mask=None, ax=None, **kwargs)


– Диаграммы рассеяния
Диаграмма рассеяния – это диаграмма с несколькими точками данных. Здесь мы видим тесную взаимосвязь между длиной лепестка и длиной чашелистика у разных видов. Ось X представляет собой длину лепестка, а ось Y – длину чашелистика в наборе данных.
Пример,
data=sns.load_dataset('iris')
sns.scatterplot(x='petal_length',y='sepal_length',hue='species',style='species',s=90,data=data)
 
Рисунок 2  – Диаграмма рассеяния, построенная с функцией scatterplot()


– Гистограммы
Гистограмма — это графическое представление распределения набора данных.
Пример 
data = np.random.randn(1000)
sns.histplot(data)
plt.show()
 
Рисунок 3 – Диаграмма рассеяния, построенная с функцией scatterplot()

– Ящик с усами (диаграмма размаха)
График, который используется для визуализации сводной статистики датасета.
Пример
data = pd.DataFrame({'Values': [10, 15, 20, 25, 30, 35, 40, 45, 50]})
sns.boxplot(x=data['Values'])
 
Рисунок 4 – Диаграмма размаха, построенная с функцией boxplot()
– Скрипичные диаграммы
Скрипичные диаграммы используются для визуализации распределения данных, отображая диапазон данных, медиану и область распределения данных.
Пример 
data=sns.load_dataset('iris')
sns.violinplot(x='species',y='petal_length',data=data,hue='species')
 
Рисунок 5 – Скрипичная диаграмма, построенная с функцией violinplot()

4. На основе выполненного анализа данных произвести выводы о динамике изменения населения по регионам, процентном соотношении населения по регионам. Выявить корреляцию между признаками.

9. Напишите программу Pandas, чтобы построить график цены акций и объема торгов Alphabet Inc. между двумя конкретными датами.
10. Напишите программу Pandas для создания графика скорректированных цен закрытия, простой скользящей средней за 30 дней и экспоненциальной скользящей средней Alphabet Inc. между двумя конкретными датами.
11. Напишите программу Pandas, чтобы создать график для визуализации дневной процентной доходности цены акций Alphabet Inc. между двумя конкретными датами.

                                                                                    Практическое занятие 11
                                                                                    Анализ данных
Описание данных
Name – название игры
Platform – платформа
Year_of_Release – год выпуска
Genre – жанр игры
NA_sales – продажи в Северной Америке (миллионы проданных копий)
EU_sales – продажи в Европе (миллионы проданных копий)
JP_sales – продажи в Японии (миллионы проданных копий)
Other_sales – продажи в других странах (миллионы проданных копий)
Critic_Score – оценка критиков (максимум 100)
User_Score – оценка пользователей (максимум 10)
Rating – рейтинг от организации ESRB (англ. Entertainment Software Rating Board). Эта ассоциация определяет рейтинг компьютерных игр и присваивает им подходящую возрастную категорию.

Задание:
1. Изучить общую информацию о данных.
2. Выполнить подготовку данных:
– обработать пропуски: удалить пропуски в столбце name, year_of_release;
– оценить количество пропусков в столбце critic_score, оставить его неизменным;
– привести столбец years_of_release к типу int;
– оценить данные в столбце  user_score, перевести этот столбец в численный тип (предварительно заменить tbd на значение None типа float);
– оценить данные в столбце rating, пропущенные данные заполнить значением «Unknown».
3. Рассчитать суммарные продажи и добавить данные в отдельный столбец.
4. Провести исследовательский анализ:
– определить количество игр, выпускаемых в разные годы, построить гистограмму распределения выпущенных игр по годам;
– выбрать платформы с наибольшими суммарными продажами и построить распределение по годам; 
– построить «ящик с усами» по продажам в зависимости от платформы;
– определить распределение продаж по жанрам, построить круговую диаграмму.
5. Определить самые популярные платформы (3 шт.), жанры (3 шт.).

