# Исследование объявлений о продаже квартир

## Описание проекта
В моем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Моя задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность.
По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма.

## Описание данных

- airports_nearest — расстояние до ближайшего аэропорта в метрах (м)
- balcony — число балконов
- ceiling_height — высота потолков (м)
- cityCenters_nearest — расстояние до центра города (м)
- days_exposition — сколько дней было размещено объявление (от публикации до снятия)
- first_day_exposition — дата публикации
- floor — этаж
- floors_total — всего этажей в доме
- is_apartment — апартаменты (булев тип)
- kitchen_area — площадь кухни в квадратных метрах (м²)
- last_price — цена на момент снятия с публикации
- living_area — жилая площадь в квадратных метрах(м²)
- locality_name — название населённого пункта
- open_plan — свободная планировка (булев тип)
- parks_around3000 — число парков в радиусе 3 км
- parks_nearest — расстояние до ближайшего парка (м)
- ponds_around3000 — число водоёмов в радиусе 3 км
- ponds_nearest — расстояние до ближайшего водоёма (м)
- rooms — число комнат
- studio — квартира-студия (булев тип)
- total_area — площадь квартиры в квадратных метрах (м²)
- total_images — число фотографий квартиры в объявлении

## Общий вывод
Изучив данные можно сделать вывод, что средняя продаваемая квартира это квартира со следующими параметрами: 
общая площадь = 57.74
жилая площадь = 33.00
площадь кухни = 10.08
количество комнат - 2
высота потолков = 2.71
этаж квартиры - 5.91
тип этажа - "другой"
общее количество этажей дома = 10.79
расстояние до близжайщего центра = 14.38 км
расстояние до близжайщего аэропрта = 28.86 км
расстояние до близжайщего парка = 493.69 м

В среднем квартира продается за 179.37 дней.

Было выявлено что количество опубликованных объявления снижается по выходным дням и в январе, мае. Больше всего объявлений публикуется в феврале, марте, апреле и ноябре. Цена не зависит от дня недели, месяца и года публикации объявления.

Самая сильная зависимость цены наблюдается от общей площади. Также на цену влияет тип этажа. Самые дорогие квартиры располагаются на "другом" этаже (средняяя стоимость квартиры на другом этаже 6.05 млн, на первом - 4.66 млн, на последнем - 5.57 млн.)

В ходе исследования было выяснено, что наибольшее количество объявлений в Санкт-Петербурге (14844 объявлений), со средней ценой квадратного метра жилья 111426.32. 

Было обнаружено, что на цену квартиры влияет удаленности о центра, средняя цена киллометра для квартир в Санкт-Петербурге равна 994980.58.

Пока в ходе исследования были потверждены некоторые очевидные закономерности: чем больше площадь квартиры тем больше ее цена. В дальнейшем можно продолжить исследования и найти закономерности между ценой и другими параметрами, представленными в датасете (количество балконов, количество парков и др.).  

В работе был посчитан один из важнейших параметров жилья - цена одного квадратного метра. Анализируя зависимость цены одного квадратного метра от других параметров можно будет найти неочевидные закономерности.
