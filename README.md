# Learning-with-teacher-project

README файл к проекту Обучение с учителем

Описание проекта и задачи:

Отток клиентов

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.
Необходимо построить модель с предельно большим значением F1-меры. Также, нужно довести метрику до 0.59. Требуется проверить F1-меру на тестовой выборке.
Дополнительно требуется измерять AUC-ROC и сравнивать её значение с F1-мерой.

Выполненные этапы проекта:
1. Первичная подготовка данных, включая удаление ненужных столбцов и обработка дубликатов;
2. Подготовили данные к машинному обучению, включая стандартизацию категориальных данных методом OHE и разделение данных на обучающую, валидационную и тестовую выборки с долями 60/20/20;
3. Провели стандартизацию числовых признаков методом StandardScaller;
4. Обучили три модели, включая DecisionTreeClassifier, RandomForestClassifier, LogisticRegression*
5. Для каждой модели создали матрицы ошибок (confusion Matrix);
6. Провели работу с выявленным дисбалансом обучающей выборки;
7. Обучили модели на сбалансированных данных;
8. Также подобрали лучшие гиперпараметры методом GridSearchCV;
9. Проверили финальную модель на адекватность и получили следующие показатели:
	•	accuracy_score константой модели: 0.7923
	•	accuracy_score финальной модели: 0.8257
	•	AUC-ROC константой модели: 0.5
	•	AUC-ROC финальной модели: 0.7556
10. Протестировали модель на тестовой выборке;

Сформировали вывод:
Наша финальная модель получила результат метрики F1 > 0.59. Модель показывает высокий показателем полноты = 0.65 (min = 0, max = 1), поэтому она с высокой вероятностью предскажит уход клиента из банка. Показатель точности не высокий = 0.56 (min = 0, max = 1) — модель верно предсказывает примерно половину ухода клиентов. Для банковских маркетологов данная модель вполне может служить хорошим инструментом для прогнозирования ухода клиента.
