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
   1. Создайте модель `todo.model.ts` и компоненту `Todo.tsx` которая будет иметь **название** задачи, **состояние**  задачи (сделана или нет), а так же 2 кнопки: `Edit` и `Delete`.
   2. Создайте компоненту со списком и в ней отобразите несколько `<Todo/>`. Для этого используйте моковые данные:
   ```json
   [
      {
         "id": "51c1c4f1-03bf-48bf-9705-9dc97ab61a76",
         "title": "delectus aut autem",
         "completed": false
      },
      {
         "id": "62aabce1-8f84-4684-90b9-2b2310cf726a",
         "title": "quis ut nam facilis et officia qui",
         "completed": false
      },
      {
         "id": "402ee516-6c72-4d16-a9a8-322069f5cf6e",
         "title": "fugiat veniam minus",
         "completed": false
      },
      {
         "id": "3b720eaf-163a-41c8-bc5e-b47f2370cd0c",
         "title": "et porro tempora",
         "completed": true
      },
      {
         "id": "3ab57b63-e789-4211-a507-6b89501bc39a",
         "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
         "completed": false
      },
      {
         "id": "09d15f18-14ea-4fd3-b75b-e57777c25b3c",
         "title": "qui ullam ratione quibusdam voluptatem quia omnis",
         "completed": false
      },
      {
         "id": "46f5bdd5-dc22-441e-b78b-e812d817cfde",
         "title": "illo expedita consequatur quia in",
         "completed": false
      },
      {
         "id": "bce9f1e0-4383-40a6-9a10-2f59d9aa1465",
         "title": "quo adipisci enim quam ut ab",
         "completed": true
      },
      {
         "id": "05da3453-89e2-4d44-8912-5b727218808c",
         "title": "molestiae perspiciatis ipsa",
         "completed": false
      },
      {
         "id": "c7034df3-eb7b-4cad-a323-3f5c6ceb9283",
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




