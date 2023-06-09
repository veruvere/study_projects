# Приоритизация гипотез и интерпретация результатов А/В-теста

Исследование для крупного интернет-магазина. Совместно с отделом маркетинга был подготовлен список гипотез для увеличения выручки. Необходимо приоритизировать гипотезы, запустить A/B-тест и проанализировать результаты. 

## Задачи:

- проанализировать гипотезы по увеличению выручки интернет-магазина
- выделить рекомендации по результатам проведения А/В-теста для выбранных гипотез

## Ход исследования
- Приоритизирование гипотез
- Предобработка данных
- Визуализация кумулятивных метрик для анализа результатов теста
- Поиск аномальных значений
- Расчет статистической значимости на сырых данных
- Удаление аномальных значений
- Расчет статистической значимости для чистых данных
- Вывод и рекомендации

## Описание данных

### Данные для первой части 
(приоритизация гипотез):

Файл /datasets/orders.csv
Hypothesis — краткое описание гипотезы;
Reach — охват пользователей по 10-балльной шкале;
Impact — влияние на пользователей по 10-балльной шкале;
Confidence — уверенность в гипотезе по 10-балльной шкале;
Efforts — затраты ресурсов на проверку гипотезы по 10-балльной шкале. Чем больше значение Efforts, тем дороже проверка гипотезы.

### Данные для второй части

Файл /datasets/orders.csv
transactionId — идентификатор заказа;
visitorId — идентификатор пользователя, совершившего заказ;
date — дата, когда был совершён заказ;
revenue — выручка заказа;
group — группа A/B-теста, в которую попал заказ.

Файл /datasets/visitors.csv. 
date — дата;
group — группа A/B-теста;
visitors — количество пользователей в указанную дату в указанной группе A/B-теста

## Статус проекта

Проект завершен.

## Вывод

- Есть статистически значимое различие по среднему количеству заказов между группами и по «сырым», и по данным после фильтрации аномалий;
- Однако нет статистически значимого различия по среднему чеку между группами ни по «сырым», ни по данным после фильтрации аномалий;
- График различия среднего количества заказов между группами сообщает, что результаты группы B намного лучше группы A;
- График различия среднего чека говорит о том, что результаты группы B превосходят группу А на 30% на момент завершения эксперимента, однако все же имеет тенденцию к снижению.
