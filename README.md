# WebbyLab Films
Это тестовое задание, в котором я познакомился с такими чудесными технологиями, как Node.js и MongoDB. 

Это веб приложение для хранения информации о фильмах.
### Функции приложения:
 - Добавления фильма;
 - Удаление фильма;
 - Показ дополнительной информации о фильме;
 - Сортировка списка фильмов в алфавитном порядке;
 - Поиск по названию фильма;
 - Поиск по имени актёра;
 - Импорт списка фильмов с текстового файла;

### Задание реализовано:
##### Front-End
**React + Material-UI**

Для клиентской части используется React и Material-UI.
Изначально писал на React+Redux, но возникли сложности связывания логики и UI, после чего было принято решение переписать всё на react hooks.
##### Back-End
**Express + MongoDB**

Для серверной части используется Node.js и MongoDB, а именно фреймворк Express и Mongoose для моделирования объектов MongoDB для Node.js

### Архитектура приложения

    ┌─ client                                     - folder with front-end 
    │   │         
    │   ├─ public                                 - app documents and assets
    │   │   ├─ index.html                         - main html file, js connection point  
    │   │   └─ ...                                  ...                  
    │   │ 
    │   ├─ src                                    - main develop folder
    │   │   │
    │   │   ├── components                        - logic and UI elements
    │   │   │   │
    │   │   │   ├─ AddFilm        
    │   │   │   │   ├─ AddFilm.jsx                - button and modal window adding film   
    │   │   │   │   ├─ AddFilm.scss               - styles
    │   │   │   │   └─ index.js                   - import/export component
    │   │   │   │
    │   │   │   ├─ Films
    │   │   │   │   ├─ FilmsList
    │   │   │   │   │   ├─ FilmsList.jsx          - UI rendering films list; sort/search logic
    │   │   │   │   │   ├─ FilmsList.scss         - styles
    │   │   │   │   │   └─ index.js               - import/export component
    │   │   │   │   │
    │   │   │   │   └─ FilmsListItem
    │   │   │   │       ├─ FilmsListItem.jsx      - UI rendering film  
    │   │   │   │       ├─ FilmsListItem.scss     - styles   
    │   │   │   │       └─ index.js               - import/export component
    │   │   │   │
    │   │   │   ├─ Search
    │   │   │   │   ├─ Search.jsx                 - UI search and radio buttons 
    │   │   │   │   ├─ Search.scss                - styles
    │   │   │   │   └─ index.js                   - import/export component
    │   │   │   │
    │   │   │   ├─ SortAlphabetically
    │   │   │   │   ├─ SortAlphabetically.jsx     - UI rendering sorting films
    │   │   │   │   ├─ SortAlphabetically.scss    - styles
    │   │   │   │   └─ index.js                   - import/export component
    │   │   │   │
    │   │   │   ├─ Title
    │   │   │   │   ├─ Title.jsx                  - UI main title
    │   │   │   │   ├─ Title.scss                 - styles
    │   │   │   │   └─ index.js                   - import/export component
    │   │   │   │
    │   │   │   └─ UploadFilmsList
    │   │   │       ├─ UploadFilmsList.jsx        - UI uploading films list (button) and logic
    │   │   │       ├─ UploadFilmsList.scss       - styles
    │   │   │       └─ index.js                   - import/export component
    │   │   │
    │   │   ├─ App.jsx                            - main react file
    │   │   ├─ App.css                            - styles
    │   │   ├─ index.js                           - React connection point 
    │   │   └─ ...                                  ...  
    │   │
    │   └─ ...                                    - configuration files (prettier, eslint, gitignore, etc)  
    │   
    ├─ server                                     - folder with back-end
    │   │
    │   ├─ models                                 - folder with database scheme
    │   │   └─ models.js                          - database scheme
    │   │
    │   ├─ routes                                 - folder with routes for connection to server
    │   │   └─ routes.js                          - routes for connection to server
    │   │
    │   ├─ server.js                              - connecting to database and port
    │   └─ ...                                    - configuration files (prettier, eslint, gitignore, etc)
    │
    └─ ...                                        - configuration files (prettier, eslint, gitignore, etc)
