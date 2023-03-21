# Todo List 

Давайте познакомимся с react и styled components!

## Подготовка окружения 
1. Установка [node.js](https://nodejs.org/en) и [npm](https://www.npmjs.com/)
   1. Переходим на [node.js](https://nodejs.org/en)
   2. Устанавливаем "Recommended For Most Users" версию
   3. Откроем консоль и выполним команды:
    ```
        node -v
    ```
    ```
        npm -v
    ```
   Если команды отработали правильно, то вы увидите версии node.js и npm соответственно

## Создание и настройка react приложения

1. Чтобы создать react приложение будем пользоваться [Create React App](https://create-react-app.dev/) но с использованием кастомного темплейта [cra-template-typescript-styled](https://www.npmjs.com/package/cra-template-typescript-styled)
   1. Для этого установим темплейт npm i cra-template-typescript-styled
   ```
   npm i cra-template-typescript-styled
   ```
   2. И используем его
   ```
   npx create-react-app todo-list --template typescript-styled
   ```
2. Темплейт содержит зависимости на [Styled Components](https://styled-components.com/) и [Prettier](https://prettier.io/). Не забудьте поставить дополнительные плагины в вашей среде разработки, чтобы комфортно с ними работать.

## Задание

Посмотрите пример того, что вам нужно сделать: [Todo List](https://todont.zachmanson.com/)

### Readonly режим
   1. Создайте модель `todo.model.tx` и компоненту `Todo.tsx` которая будет иметь **название** задачи, **состояние**  задачи (сделана или нет), а так же 2 кнопки: `Edit` и `Delete`.
   2. Создайте компоненту со списком и в ней отобразите несколько `<Todo/>`. Для этого используйте моковые данные:
   ```json
   [
      {
         "id": 1,
         "title": "delectus aut autem",
         "completed": false
      },
      {
         "id": 2,
         "title": "quis ut nam facilis et officia qui",
         "completed": false
      },
      {
         "id": 3,
         "title": "fugiat veniam minus",
         "completed": false
      },
      {
         "id": 4,
         "title": "et porro tempora",
         "completed": true
      },
      {
         "id": 5,
         "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
         "completed": false
      },
      {
         "id": 6,
         "title": "qui ullam ratione quibusdam voluptatem quia omnis",
         "completed": false
      },
      {
         "id": 7,
         "title": "illo expedita consequatur quia in",
         "completed": false
      },
      {
         "id": 8,
         "title": "quo adipisci enim quam ut ab",
         "completed": true
      },
      {
         "id": 9,
         "title": "molestiae perspiciatis ipsa",
         "completed": false
      },
      {
         "id": 10,
         "title": "illo est ratione doloremque quia maiores aut",
         "completed": true
      }
  ]
   ```
   3. Отобразите счётчик **всех** задач над списком. Для этого используйте отдельную компоненту.

### Удаление и Создание Todo
   1. Добавьте возможность удаления элемента из списка по нажатию на кнопку `Delete`. Число в счётчике должно меняться при удалении.
   2. Создайте новую компоненту и добавьте поле ввода текста и кнопку `Add`
   3. При нажатии на кнопку `Add`, если текстовое поле заполнено, создайте новый элемент в списке и обновите счётчик задач. Используйте [uuid](https://www.npmjs.com/package/uuid) для генерации уникльного id.

### Изменение Todo
   1. Добавьте возможность менять **состояние** задачи (сделана или нет)
   2. Добавьте возможность включать и выключать режим редактирования **Названия** задачи
      1. При клике на кнопку `Edit` Должно появиться текстовое поле и кнопки `Save`/`Cancel`. Кнопки `Edit` и `Delete`, а так же чекбокс состояния должны изчезнуть.
      2. При нажатии на кнопку `Save`, если поле заполнено, название задачи должно измениться. При нажатии на `Cancel`, название задачи должно вернуться в исходное состоняие.

### Фильтрация Todos
   1. Добавьте три кнопки фильтрации: `Show All Tasks`, `Show Active Tasks`, `Show completed Tasks`
      1. При нажатии на каждую из кнопок список должен меняться соответствующим образом
      2. Подсвечивайте активный фильтр
   

## Дополнительные материалы

1. [React](https://ru.reactjs.org/)
2. [Styled components](https://habr.com/ru/post/591381/)




