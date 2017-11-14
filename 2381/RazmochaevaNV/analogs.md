## Сравнение аналогов

Для решения поставленной задачи можно использовать различные подходы и методы. Далее представлена группировка методов на три основные группы.

### Формализованные методы

В [1] под формализованными методами подразумевают следующие: 

- методы экстраполяции, 
- методы из теории массового обслуживания, 
- статистические методы.

### Методы прогнозирования

В [2,3] выделяют в отдельную группу методы прогнозирования и включают сюда следующие: 

- балансовые методы, 
- методы из теории исследования операций, 
- эконометрические методы.

К последней группе относят методы работы с экономическими параметрами и характеристиками [3].

### Методы оптимизации

Методы оптимизации широко используются в задачах анализа поведения целевых функций. Например, методы поиска экстремума функции (градиентный спуск и др.).

## Критерии сравнения аналогов

### Нелинейность

Формирование ассортимента - нелинейный процесс (показано на примере анализа спроса в [2,3]). Нелинейность процесса формирования ассортимента обязательно нужно учитывать.

### Математическая модель

Разработка математической модели, поиск аналитического вида функции процесса формирования ассортимента - невыполнимая задача [1], поэтому нужен инструмент, не требующий наличие математической модели.

### Использование опыта

При формировании ассортимента анализируется большое количество данных о продажах - так называемый опыт продаж, который играет главную роль при принятии решений.

## Таблица сравнения по критериям

|                       | Формализованные методы | Методы прогнозирования | Методы оптимизации | Нейронные сети |
| --------------------- | ---------------------- | ---------------------- | ------------------ | -------------- |
| Учет нелинейности     | Нет                    | Есть                   | Есть               | Есть           |
| Математическая модель | Нужна                  | Нужна                  | Нужна              | Не нужна       |
| Использование опыта   | Нет                    | Есть                   | Нет                | Есть           |



## Выводы по итогам сравнения

По итогам сравнения можно сделать вывод, что для решения поставленной задачи формирования ассортимента товаров подходящим инструментом является нейронная сеть. Использование данного инструмента позволяет моделировать нелинейность поведения исследуемого процесса, не требует наличия математической модели процесса (или аналитического вида функции), и, главное, позволяет в полной мере использовать накопленный опыт продаж.

## Источники

1. Тихонов Э.Е. Методы прогнозирования в условиях рынка: учебное пособие. – Невинномысск, 2006. – 221 с.
2. Бугорский В.Н., Никитин Н.А. Нейронные сети в управлении розничной торговлей // IT-менеджмент. Реальная коммерция. Прикладная информатика 2006. № 2. С. 34 - 41.
3. Ибрагимов А.У., Ибрагимова Л.А., Гильмуллина Г.И. Применение методов искусственного интеллекта для анализа и прогноза товарооборота розничного торгового предприятия // Вестник Самарского государственного аэрокосмического университета 2012. № 1 (32). С. 233-241.