﻿# <Название статьи>
## Аннотация



## Введение

Современные технологии предлагают больше возможностей в сфере образования. Большая популярность мобильных технологий предоставяет удобный инструмент для интерактивного обучения посредством мобильных приложений. На данный момент существует множество платформ, которые позволяют создавать outdoor-квесты, в которых пользователям предлагается решать интеллектуальные загадки, разгадывать местоположения позновательных мест. Однако у данных платформ существуют ограничения, главное из которых - закрытый код, что останавливает их развитие. Целью данной работы является проектирование архитектуры платформы с открытым исходным кодом, которая позволит создавать обучающие мобильные приложения с уникальными наборами outdoor квестами. Для этого в статье будет проведет анализ аналогичных приложений и платформ, предложена собственная архитектура платформы и рассмотрен алгоритм автоматической генерации квестов.

## Сравнение аналогов

В данном разделе сравниваются существующие аналогичные приложения и платформы.

### Аналоги приложений
#### Geocaching

Приложение, предлагающее найти при помощи карты и меток на них тайники и интересные места в реальной жизни. Активно используется туристами, интерес поддерживается при помощи статистики и соревновательной составляющей.

#### Путеводитель iSpbGuide

Приложение, являющееся путеводителем по историческим и культурным достопримечательностям по Санкт-Петербургу. Содержит в себе текстовую, графическую и звуковую информацию по достопримечательностям.

#### Blippar

Приложение, позволяющее получить информацию о любых вещах при помощи дополненной реальности и распознавания изображений. При помощи данных с видеокамеры телефона можно получить информацию о многих реальных вещах.

#### Критерии сравнения аналогов приложений

##### Количество установок на Google Play

Количество установок показывает интерес к приложениям подобного рода.

##### Расход батареи за час

Расход энергии для мобильных устройств очень актуален, так как батарейка имеет ограниченный запас и необходимо минимизировать потребление энергии приложением.

##### Количество квестов/информации

Важный критерий, показывающий информационную ценность приложения, наличие в нём контента для использования.

#### Таблица сравнения по критериям

Приложение | Количество установок на Google Play | Размер установленного приложения | Количество квестов/информации
---------- | ----------------------------------- | -------------------------------- | -----------------------------
Geocaching | 5 000 000–10 000 000 | 41,91 | > 1 000 000
Путеводитель iSpbGuide | 100 000–500 000 | 28,32 МБ | > 12
Blippar | 1 000 000–5 000 000 | 85,47 МБ | > 10 000 000

#### Выводы по итогам сравнения

В результате сравнения существующих аналогов можно сказать, что интерес к приложениям подобного рода довольно большой, значительно зависит от качества приложения, в том числе размера. Если приложение слишком большое - пользователям будет сложнее его скачать.

### Аналоги платформ
#### Surprise Me

Платформа для создания квестов в виде персональных мобильных приложений. Позволяет создавать различные квесты, в том числе по посещению определенных мест. Большинство созданных квестов платные.

#### OUTDOOR ADVENTURE QUEST

Аналогичная платформа, предоставляющая возможность создать собственный outdoor-квест. Созданные варианты ориентируются на путешественников, велосипедистов и групп людей, желающих устроить для себя проверку возможностей.

#### 12CODES

Это интернет-сервис для проведения квестов. Он подходит почти для любых целей - от ночных автоквестов до городских экскурсий.

#### Критерии сравнения аналогов приложений

##### География квестов

Важный критерий, показывающий развитие платформы - чем большую площадь охватывают квесты, тем больше возможностей у пользователей платформы.

##### Возможность создания собственного приложения

Создание квестов это важный момент, но наличие возможности создания собственного приложения даст пользователям большую свободу и гибкость.

##### Веб-интерфейс для создания квестов и приложений

Наличие веб-интерфейса очень важный элемент, который должен присутствовать у платформы, если она нацелена на обычных пользователей, а не только программистов.

#### Таблица сравнения по критериям

Платформа | География квестов | Возможность создания собственного приложения | Веб-интерфейс для создания квестов и приложений
---------- | ----------------------------------- | -------------------------------- | -----------------------------
Surprise Me | Большие города России | Отсутствует | Есть
OUTDOOR ADVENTURE QUEST | Весь мир | Отсутствует | Отсутствует
12CODES | Города России | Отсутствует | Есть

#### Выводы по итогам сравнения

Во всех платформах отсутствует возможность создания собственного приложения, что сильно ограничивает пользователей таких платформ.

### Источники

1. [Geocaching](https://play.google.com/store/apps/details?id=com.groundspeak.geocaching.intro)
2. [Путеводитель iSpbGuide](https://play.google.com/store/apps/details?id=iSpbGuide.com)
3. [Blippar](https://play.google.com/store/apps/details?id=com.blippar.ar.android)
4. [Surprise Me](https://surprizeme.ru/)
5. [OUTDOOR ADVENTURE QUEST](http://outdooradventurequest.com/)
6. [12CODES](https://12codes.ru/)

## Архитектура платформы

В этом разделе рассматривается архитектура будущей платформы. На рисунке 1 представлена схема этой архитектуры.

![Архитектура платформы](https://lh4.googleusercontent.com/NcIniONajW8Lb6ItANvsnzps_tYHAX-kXfxA11mk55B-XopqNvITcfCMzR5NE7QsC_BJdTzfqMN4Sa5oIHNy=w1920-h988-rw)
Рис 1. Архитектура платформы

### Web-interface

Для администрирования квестов и приложений пользователям нужен удобный интерфейс, который будет выполнен в виде сайта, к которому сможет получить доступ любой желающий. В нём также будут присутствовать автоматический генератор квестов, подробнее о котором рассказано в следующем разделе, и сборщик мобильных приложений с настройками пользователя.

### Генератор квестов

Принцип работы алгоритма генерации уникальных квестов будет многоступенчатым. На вход генератору будут подаваться исходные данные - максимальное количество мест в квесте, теги, определяющие тематику квестов (например "Пётр 1", "Санкт-Петербург"). После чего будет происходить перебор всех возможных вариантов. На следующем этапе будут отсеиваться варианты, которые не подходят под главный критерий, чтобы квест был наиболее прямолинейным, не возвращая игрока в предыдущие места. Данный этап реализуется при помощи подсчета углов между тремя местами, если угол острее определенного порога - то квест не подходит. Наиболее оптимистичный вариант, когда все углы будут по 180 градусов, это будет означать, что маршрут квеста находится на одной прямой. На последнем этапе оставшиеся квесты будут отсортированны по длинне маршрута, рассчитываемого специальными способами.

### База данныз (MongoDB)

Для хранения всей информации о приложения, пользователях и квестах будет использоваться нереляционная СУБД - MongoDB. Именно документоориентированность данной СУБД позволит хранить и быстро обрабатывать гео-данные и упростит обмен информацией с приложениями за счет использование формата JSON.

### Сгенерированные приложения

Готовые приложения пользователей будет связываться напрямую с БД и использовать полученные данные, чтобы предоставить пользователям возможность выполнять интересные, развлекающие и обучающие квесты.

## Заключение

В результате данной работы была спроектированна и представлена архитектура платформы с открытым исходным кодом, которая позволяет создавать образовательные мобильные приложения с уникальным набором outdoor-квестов.

## Список литературы

1. Doellner J. Service-Oriented Geovisualization for Geodesign //Proceedings of Digital Landscape Architecture. – 2014. – С. 43-45.
2. Baldauf M., Musialski P. A device-aware spatial 3D visualization platform for mobile urban exploration //The fourth international conference on mobile ubiquitous computing, systems, services and technologies (UBICOMM 2010), IARIA. – 2010.
3. Follin J. M. et al. Visualization of multi-resolution spatial data in mobile system //Proceedings of 1st International Workshop on Ubiquitous GIS. – 2004.
4. Заславский М.М., Мокрецов Р. Платформа для конструирования мобильных образовательных приложений на базе LBS-платформы GEO2TAG // Современные технологии в теории и практике программирования: материалы научно-практической конференции студентов, аспирантов и молодых ученых - 2017. - С. 67-70