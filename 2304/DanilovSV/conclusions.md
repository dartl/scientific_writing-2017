## Выводы

На основании обзора существующих подходов к решению поставленной проблемы и анализа их достоинств и недостатков был разработан и встроен в существующую систему алгоритм ранжирования выдачи виртуального ассистента.

Эффективность работы алгоритма по времени обеспечивается тем, что для получения ответа от обученной модели, необходимо только извлечь признаки из текстового запроса. Такие признаки (например, tf-idf) извлекаются за пренебрежительно малое время.

Разработанное приложение позволяет поддерживать до 1600 одновременных обращений пользователей при использовании кластера из 10 серверов. Дальнейшая работа будет направлена на улучшение показателей качества модели и общей производительности приложения.
