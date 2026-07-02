# Анализ данных интернет-магазина (Online Retail)

## Описание проекта
Анализ транзакций британского интернет-магазина подарков за период с декабря 2010 по декабрь 2011 года.

**Цель:** провести полный цикл анализа данных: от очистки до сегментации клиентов и построения интерактивного дашборда.

**Инструменты:** Python (Jupyter), Power BI, Git

---

## Этапы работы

### 1. Очистка и предобработка данных (Python)
- Удаление пропусков в `CustomerID` и `Description`
- Фильтрация отрицательных значений `Quantity` и `UnitPrice`
- Обработка отмен заказов (счета с префиксом 'C')
- Создание признака `Revenue = Quantity * UnitPrice`

### 2. Feature Engineering
- Извлечение из даты: месяц, день недели, час, признак выходного дня
- Агрегация до уровня заказа для расчёта среднего чека

### 3. RFM-анализ и сегментация клиентов
- Расчёт Recency, Frequency, Monetary для каждого клиента
- Присвоение RFM-баллов (квартили)
- Выделение сегментов: Champions, Loyal, Promising, At Risk, Lost

### 4. Построение дашборда в Power BI
- Модель «Звезда»: 1 таблица фактов и 3 таблицы измерений
- Ключевые метрики: общая выручка, количество заказов, средний чек
- Три страницы дашборда: «Обзор продаж», «Товарный анализ», «Клиентская аналитика»

---

## Ключевые выводы
1. **Топ-страна по выручке** — Великобритания (~90% продаж)
2. **Сезонный пик** — ноябрь 2011 года (подготовка к Рождеству)
3. **Сегмент Champions** — всего 10% клиентов, но приносят ~60% выручки
4. **Сегмент At Risk** — требуют маркетингового воздействия (скидки, письма)

---

## Демонстрация дашборда
<img width="1320" height="746" alt="image" src="https://github.com/user-attachments/assets/90c213c7-f9d3-44d9-929b-014627a111a6" />

<img width="1323" height="749" alt="image" src="https://github.com/user-attachments/assets/d907aa08-4d6c-409b-bb52-da67273246b8" />

<img width="1312" height="750" alt="image" src="https://github.com/user-attachments/assets/0c16719b-f795-4763-a793-0f1a5e49d3bc" />

---

## Как запустить проект

### 1. Jupyter Notebook
```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook notebooks/ecommerce_analysis.ipynb
```

### 2. Power BI
Откройте файл `powerbi/ecommerce_dashboard.pbix` в Power BI Desktop.

---

## Ссылки
- [Датасет на Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
