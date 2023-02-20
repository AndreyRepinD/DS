# Отток клиентов
Из "Бета-Банка" понемногу каждый месяц уходят клиенты. Так как сохранить текузих клиентов дешевле, чем привлекать новых, то нужно спрогнозировать уйдет ли клиент из банка или нет.
**Цель исследования** — построить модель, которая спрогнозирует уход клиента.

**Ход исследования**.

Исследование пройдёт в пять этапов:
1. Подготовка данных.
2. Исследовать качество разных моделей, меняя гиперпараметры. В работе используются 3 модели: DecisionTreeClassifier, RandomForestClassifier и LogisticRegression
3. Борба с дисбалансом
3. Проверить качество модели на тестовой выборке.
5. Проверить модели на вменяемость. 

**Описание данных**.

Данные находятся в файле /datasets/Churn.csv (англ. «отток клиентов»).

Признаки
1. `RowNumber` — индекс строки в данных
2. `CustomerId` — уникальный идентификатор клиента
3. `Surname` — фамилия
4. `CreditScore` — кредитный рейтинг
5. `Geography` — страна проживания
6. `Gender` — пол
7. `Age` — возраст
8. `Tenure` — сколько лет человек является клиентом банка
9. `Balance` — баланс на счёте
10. `NumOfProducts` — количество продуктов банка, используемых клиентом
11. `HasCrCard` — наличие кредитной карты
12. `IsActiveMember` — активность клиента
13. `EstimatedSalary` — предполагаемая зарплата
Целевой признак:
1. `Exited` — факт ухода клиента

Источник данных: [https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling](https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling)
<h1>Содержание<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Подготовка-данных" data-toc-modified-id="Подготовка-данных-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Подготовка данных</a></span></li><li><span><a href="#Исследование-задачи" data-toc-modified-id="Исследование-задачи-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Исследование задачи</a></span></li><li><span><a href="#Борьба-с-дисбалансом" data-toc-modified-id="Борьба-с-дисбалансом-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Борьба с дисбалансом</a></span></li><li><span><a href="#Тестирование-модели" data-toc-modified-id="Тестирование-модели-4"><span class="toc-item-num">4&nbsp;&nbsp;</span>Тестирование модели</a></span></li></ul></div>
