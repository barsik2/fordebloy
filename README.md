Конечно! Вот пример README для вашего проекта. Он включает описание, установку, использование, а также технические детали.

---

# Network Visualization App

Это приложение позволяет визуализировать сети с узлами и рёбрами, а также предоставляет функционал для работы с ними: создание, редактирование и удаление узлов и рёбер, а также отображение различных метрик сети, таких как степень узлов и центральность.

## Описание

Данное приложение использует библиотеку **vis-network** для построения визуализаций графов и предоставляет интерфейс для работы с графами с помощью **React**. Основные возможности включают:

- Визуализация узлов и рёбер.
- Создание, обновление и удаление узлов и рёбер через контекстное меню.
- Интерактивные функции: выделение узлов, просмотр степеней и центральности.
- Обработчики событий для взаимодействия с графом (выбор узлов, контекстные меню и т. д.).

## Структура проекта

- `NetworkChart.js` — основной компонент, отвечающий за визуализацию графа, обработку событий и контекстное меню.
- `networkChart.css` — стили для компонента `NetworkChart`.
- `App.js` — корневой компонент приложения, подключающий `NetworkChart`.
- `package.json` — файл зависимостей и настроек проекта.

## Установка

1. **Клонируйте репозиторий:**

    ```bash
    git clone https://github.com/yourusername/network-visualization-app.git
    cd network-visualization-app
    ```

2. **Установите зависимости:**

    ```bash
    npm install
    ```

3. **Запустите приложение:**

    ```bash
    npm start
    ```

    Приложение будет доступно по адресу `http://localhost:3000`.

## Использование

1. **Добавление узлов:**
    - Щелкните правой кнопкой мыши в области графа и выберите "Create Node". В появившемся диалоговом окне укажите данные для нового узла (например, метку и тип).
    
2. **Обновление узлов:**
    - Щелкните правой кнопкой мыши по существующему узлу и выберите "Update". Отредактируйте его данные в появившемся диалоговом окне.

3. **Удаление узлов:**
    - Щелкните правой кнопкой мыши по узлу и выберите "Delete". Узел будет удалён из графа.

4. **Добавление рёбер:**
    - Щелкните правой кнопкой мыши в области графа и выберите "Create Edge". Укажите параметры рёбра, включая тип, веса и направленность.

5. **Обновление рёбер:**
    - Щелкните правой кнопкой мыши по существующему ребру и выберите "Update". Измените параметры рёбра в диалоговом окне.

6. **Удаление рёбер:**
    - Щелкните правой кнопкой мыши по ребру и выберите "Delete".

7. **Просмотр степени и центральности узлов:**
    - При наведении на узел отображаются его степень (количество связанных рёбер) и центральность (в данный момент используется заглушка).

8. **Просмотр кратчайших путей (если они есть):**
    - Кратчайшие пути, если они существуют, будут отображаться красным цветом.

## Технические особенности

### Используемые библиотеки

- **React**: Основной фреймворк для создания пользовательского интерфейса.
- **vis-network**: Библиотека для визуализации графов и сетей.
- **vis-data**: Библиотека для работы с данными графов в формате DataSet.
- **Material-UI**: Библиотека компонентов для React, использующая Material Design, для создания интерфейса.

### Структура данных

1. **Узлы (nodes)**: Каждый узел содержит уникальный идентификатор (`id`), метку (`label`) и тип (`type`).
2. **Рёбра (edges)**: Каждое ребро содержит два узла, с которыми оно соединено (`from`, `to`), веса (`weights`), а также тип (`type`) и направление (`directed`).

Пример структуры данных для узлов и рёбер:

```javascript
const nodes = [
  { id: 1, label: 'Node 1', type: 'tp1' },
  { id: 2, label: 'Node 2', type: 'tp2' },
  { id: 3, label: 'Node 3', type: 'tp1' }
];

const edges = [
  { from: 1, to: 2, weights: '5', directed: true, type: 'edge1' },
  { from: 2, to: 3, weights: '3', directed: false, type: 'edge2' }
];
```

### Основные функции

- **`onNodeClick`**: Функция, которая срабатывает при клике на узел.
- **`onDeleteNode`**: Функция для удаления узла.
- **`onUpdateNode`**: Функция для обновления данных узла.
- **`onAddNode`**: Функция для добавления нового узла.
- **`onDeleteEdge`**: Функция для удаления ребра.
- **`onUpdateEdge`**: Функция для обновления данных рёбер.
- **`onAddEdge`**: Функция для добавления нового рёбра.

## Технологии

- **React** - для создания компонента с состоянием и обработчиками событий.
- **vis-network** - для визуализации сети и графов.
- **Material-UI** - для создания интерфейса и взаимодействий с пользователем (диалоговые окна, контекстное меню и т.д.).
- **JavaScript (ES6)** - для логики работы приложения.

## Лицензия

Этот проект распространяется под лицензией MIT. Подробности можно найти в файле `LICENSE`.

---

Пожалуйста, не забудьте адаптировать URL-адрес в разделе установки и внести другие изменения, если это необходимо для вашего проекта.

