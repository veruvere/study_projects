# Исследование рынка общественного питания Москвы для инвесторов

Инвесторы из фонда «Shut Up and Take My Money» решили попробовать себя в новой области и открыть заведение общественного питания в Москве. Заказчики ещё не знают, что это будет за место: кафе, ресторан, пиццерия, паб или бар, — и какими будут расположение, меню и цены. 

Цель аналитики:

- помочь инвесторам выбрать максимально выгодное расположение для открытия нового заведения общественного питания.

## Задача:

- выявить интересные особенности, которые помогут инвесторам принять решение об открытии.

## Ход исследования
- Изучаем информацию о датасете
- Предобработка данных
- Анализ данных:
    - кол-во объектов по категориям (распределение)
    - кол-во посадочных мест по категориям
    - соотношение сетевых и несетевых заведений
    - выявить том-15 популярных заведений
    - админ районы
    - распередение средних рейтингов
- Построение и изучение фоновой картограммы:
    - отобразить все заведения с помощью кластеров
    - топ 15 улиц по кол-ву заведений
    - хороплет медианы средних чеков
    - доп исследование
- Мини-исследование по кофейням Москвы с целью сформировать рекомендации по его открытию

## Описание данных

Файл moscow_places.csv:

name — название заведения;

address — адрес заведения;

category — категория заведения, например «кафе», «пиццерия» или «кофейня»;

hours — информация о днях и часах работы;

lat — широта географической точки, в которой находится заведение;

lng — долгота географической точки, в которой находится заведение;

rating — рейтинг заведения по оценкам пользователей в Яндекс Картах (высшая оценка — 5.0);

price — категория цен в заведении, например «средние», «ниже среднего», «выше среднего» и так далее;

avg_bill — строка, которая хранит среднюю стоимость заказа в виде диапазона, например:

   - «Средний счёт: 1000–1500 ₽»;
   - «Цена чашки капучино: 130–220 ₽»;
   - «Цена бокала пива: 400–600 ₽».
   - и так далее;
   
middle_avg_bill — число с оценкой среднего чека, которое указано только для значений из столбца avg_bill, начинающихся с подстроки «Средний счёт»:

   - Если в строке указан ценовой диапазон из двух значений, в столбец войдёт медиана этих двух значений.
   - Если в строке указано одно число — цена без диапазона, то в столбец войдёт это число.
   - Если значения нет или оно не начинается с подстроки «Средний счёт», то в столбец ничего не войдёт.
   
middle_coffee_cup — число с оценкой одной чашки капучино, которое указано только для значений из столбца avg_bill, начинающихся с подстроки «Цена одной чашки капучино»:

   - Если в строке указан ценовой диапазон из двух значений, в столбец войдёт медиана этих двух значений.
   - Если в строке указано одно число — цена без диапазона, то в столбец войдёт это число.
   - Если значения нет или оно не начинается с подстроки «Цена одной чашки капучино», то в столбец ничего не войдёт.
   
chain — число, выраженное 0 или 1, которое показывает, является ли заведение сетевым (для маленьких сетей могут встречаться ошибки):

   - 0 — заведение не является сетевым
   - 1 — заведение является сетевым
   
district — административный район, в котором находится заведение, например Центральный административный округ;

seats — количество посадочных мест.

## Статус проекта

Проект завершен.

## Вывод

- Одним их самых привлекательных вариантов для открытия является бар или паб - по количеству их в Москве не так уж много, всего 9%.
- Перспективный район для открытия бара - Северный. Там самый высокий чек и немного баров - всего 41.
- У таких заведений обычно самый высокий рейтинг и чек - ~4.4 и 1572.81р (На севере Москвы).
