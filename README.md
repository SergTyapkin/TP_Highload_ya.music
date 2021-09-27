# Архитектура высоконагруженного веб-сервиса
----------------
## Yandex.music
Яндекс.Музыка - популярный сервис по прослушиванию музыки
----------------
## Статистика
* Кол-во зарегистрированных пользователей: [>3 млн.](https://vc.ru/media/96460-chislo-podpischikov-yandeks-muzyki-vyroslo-v-tri-raza-za-poltora-goda-i-dostiglo-3-mln)

### План-график
Занятие  | Готовность
---------| --------------------------------
Лекция 1 | Выдача задания
Лекция 2 | Выбор темы и целевой аудитории
Лекция 3 | Утверждение темы преподавателем
Лекция 4 | Расчет нагрузки
Лекция 5 | Логическая схема БД
Лекция 6 | Физическая схема БД
Лекция 7 | Выбор технологий
Лекция 8 | Схема проекта
РК 3     | Полная готовность
## 1. Тема и целевая аудитория
Студент должен выбрать тип сервиса, функционал MVP который он будет проектировать и целевую аудиторию (размер и местоположение).
### Требования к теме
* Сервис должен иметь реальные аналоги доказывающие существование рыночной ниши для такого типа сервиса и потенциальный размер аудитории
* Сервис должен быть достаточно сложным чтобы его архитектура не была тривиальной (пример тривиальной архитектуры: новостной сайт)
* Разрешается не более 3-х сервисов с одинаковой темой но диверсифицированных между собой (варианты занимаются в порядке очереди)
* в MVP нужно положить ключевой функционал сервиса
### Требования к целевой аудитории
* Аудитория должна быть достаточно большой чтобы сервис получился высоконагруженным. Минимум - 1 млн пользователей в день. Рекомендуемое значение - аудитория реального аналога, общемировая или на локальном рынке.
* Необходимо указать размер и местоположение целевой аудитории (Примеры: 100 млн в месяц Россия, 200 млн в месяц Северная Америка и Европа)
## 2. Расчет нагрузки
Необходимо пересчитать аудиторные метрики в ключевые продуктовые и технические метрики.
### Продуктовые метрики
* Месячная аудитория - обязательно
* Дневная аудитория - обязательно
* Средний размер хранилища пользователя (по типам, там где существенно)
* Среднее количество действий пользователя по типам в день (типы запросов выбираем на основании выбраного функционала MVP)
Оформить в виде сводной таблицы.
### Технические метрики
* Размер хранения в разбивке по типам данных (в Тб) - для существенных блоков данных
* Сетевой трафик
** Пиковое потребление в теченнии суток (в Гбит/с) - разбивка по существенным типам трафика (для выбора сетевых интерфейсов)
** Суммарный суточный (Гбайт/сутки) - разбивка по существенным типам трафика (опционально, для подсчета стоимости хостинга)
* RPS в разбивке по типам запросов (запросов в секунду) - для основных запросов
Оформить в виде сводной таблицы.
## 3. Логическая схема
### Требования
* Картинка со списком таблиц, полей и связей между ними без привязки к конкретным базам и шардингу
## 4. Физическая схема
### Требования
* Картинка со списком таблиц, полей и связей между ними с привязкой к конкретным базам, с указанием индексов и схемы шардинга
## 5. Технологии
Сводная таблица: технология, область примерения, мотивационная часть
## 6. Схема проекта
Схема взаимодействия сервисов внутри проекта (картинка). Должно быть описано как ходят потоки данных, как устроена балансировка (внутренняя и внешняя).
## 7. Список серверов
Таблица с конфигурациями, количеством серверов и сервисами расположенными на них. В случае использования kubernetes или иной виртуализации, список контейнеров с аллокацией ресурсов.
