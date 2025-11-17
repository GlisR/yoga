# Документ дизайна

## Обзор

Сайт йоги представляет собой простой многостраничный веб-сайт, состоящий из 5 HTML-страниц, связанных навигационным меню. Сайт использует W3.CSS фреймворк для стилизации и выполнен в теплых, светлых и нежных тонах. Дизайн ориентирован на простоту и понятность для начинающих веб-разработчиков.

## Архитектура

### Структура проекта

```
yoga-website/
├── index.html              # Главная страница
├── books.html              # Страница с книгами
├── music.html              # Страница с музыкой
├── videos.html             # Страница с видео
├── schedule.html           # Страница с расписанием и контактами
├── styles/
│   └── custom.css          # Дополнительные пользовательские стили
├── images/                 # Папка с изображениями
│   ├── dancer.jpeg
│   ├── meditation.jpeg
│   ├── pigeon.jpeg
│   └── scorpion.jpeg
└── music/                  # Папка с аудиофайлами
    └── 01_1_Purnima_Namashkar_Chinmaya_Dunster_www_oum_ru.mp3
```

### Технологический стек

- **HTML5**: Структура страниц
- **CSS3**: Стилизация (через W3.CSS)
- **W3.CSS**: CSS фреймворк (подключается через CDN)
- **Google Maps Embed API**: Встроенная карта
- **YouTube Embed**: Встроенные видео

## Компоненты и интерфейсы

### 1. Навигационное меню

**Описание**: Общий компонент навигации, присутствующий на всех страницах.

**Структура**:
```html
<nav class="w3-bar w3-light-grey">
  <a href="index.html" class="w3-bar-item w3-button">Home</a>
  <a href="books.html" class="w3-bar-item w3-button">Books</a>
  <a href="music.html" class="w3-bar-item w3-button">Music</a>
  <a href="videos.html" class="w3-bar-item w3-button">Videos</a>
  <a href="schedule.html" class="w3-bar-item w3-button">Schedule & Contact</a>
</nav>
```

**Стилизация**:
- Использует классы W3.CSS: `w3-bar`, `w3-bar-item`, `w3-button`
- Цвет фона: светлый (w3-light-grey или кастомный теплый оттенок)
- Активная страница может быть выделена классом `w3-theme`

### 2. Главная страница (index.html)

**Описание**: Приветственная страница с информацией о преподавателе и философии йоги.

**Компоненты**:
- Заголовок с приветствием
- Секция "О преподавателе"
- Фотографии йоги (из папки images/)
- Контактная информация (Instagram, телефон, мессенджеры)
- Иконки мессенджеров: Telegram, WhatsApp, Facebook

**Структура**:
```html
<header class="w3-container w3-center">
  <h1>Welcome to [Имя] Yoga Studio</h1>
  <p>Find your inner peace</p>
</header>

<section class="w3-container">
  <h2>About Me</h2>
  <img src="images/meditation.jpeg" class="w3-image">
  <p>[Текст о преподавателе]</p>
</section>

<section class="w3-container">
  <h2>Contact Me</h2>
  <p>Instagram: @yogastudio</p>
  <p>Phone: +380 XX XXX XXXX</p>
  <div>
    <a href="#">Telegram</a>
    <a href="#">WhatsApp</a>
    <a href="#">Facebook</a>
  </div>
</section>
```

### 3. Страница книг (books.html)

**Описание**: Коллекция рекомендованных книг по йоге.

**Компоненты**:
- Заголовок страницы
- Сетка карточек книг (3-4 книги)
- Каждая карточка содержит: изображение, название, автор, краткое описание

**Структура**:
```html
<div class="w3-row-padding">
  <div class="w3-third">
    <div class="w3-card">
      <img src="images/pigeon.jpeg" class="w3-image">
      <div class="w3-container">
        <h3>Book Title</h3>
        <p>Author Name</p>
        <p>Short description...</p>
      </div>
    </div>
  </div>
  <!-- Повторить для других книг -->
</div>
```

### 4. Страница музыки (music.html)

**Описание**: Плейлист с музыкой для медитации и йоги.

**Компоненты**:
- Заголовок страницы
- HTML5 аудиоплеер
- Список треков

**Структура**:
```html
<div class="w3-container">
  <h2>Meditation Music</h2>
  
  <div class="w3-panel">
    <h3>Track 1: Purnima Namashkar</h3>
    <audio controls class="w3-border">
      <source src="music/01_1_Purnima_Namashkar_Chinmaya_Dunster_www_oum_ru.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
  </div>
  
  <!-- Можно добавить больше треков -->
</div>
```

### 5. Страница видео (videos.html)

**Описание**: Встроенные видео тренировок с YouTube.

**Компоненты**:
- Заголовок страницы
- 2-3 встроенных видео YouTube
- Описание каждого видео

**Структура**:
```html
<div class="w3-container">
  <h2>Yoga Video Tutorials</h2>
  
  <div class="w3-panel">
    <h3>Morning Yoga Flow</h3>
    <iframe width="560" height="315" 
            src="https://www.youtube.com/embed/VIDEO_ID" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
    </iframe>
    <p>Description of the video...</p>
  </div>
  
  <!-- Повторить для других видео -->
</div>
```

### 6. Страница расписания и контактов (schedule.html)

**Описание**: Расписание занятий в таблице и контактная информация с картой.

**Компоненты**:
- Таблица расписания
- Карта Google Maps
- Адрес и контактная информация

**Структура таблицы**:
```html
<div class="w3-container">
  <h2>Class Schedule</h2>
  
  <table class="w3-table w3-striped w3-bordered">
    <thead>
      <tr class="w3-light-grey">
        <th>Day</th>
        <th>Time</th>
        <th>Class Type</th>
        <th>Level</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Monday</td>
        <td>10:00 - 11:30</td>
        <td>Hatha Yoga</td>
        <td>Beginner</td>
      </tr>
      <!-- Больше строк -->
    </tbody>
  </table>
</div>
```

**Структура карты**:
```html
<div class="w3-container">
  <h2>Location</h2>
  
  <iframe src="https://www.google.com/maps/embed?pb=..." 
          width="100%" 
          height="400" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy">
  </iframe>
  
  <div class="w3-panel">
    <p><strong>Address:</strong> [Адрес центра йоги]</p>
    <p><strong>Phone:</strong> +380 XX XXX XXXX</p>
    <p><strong>Email:</strong> yoga@example.com</p>
    <p><strong>Telegram:</strong> @yogastudio</p>
    <p><strong>WhatsApp:</strong> +380 XX XXX XXXX</p>
    <p><strong>Instagram:</strong> @yogastudio</p>
  </div>
</div>
```

## Модели данных

Поскольку сайт статический (только HTML/CSS), модели данных не используются. Все данные жестко закодированы в HTML.

### Контент для заполнения

**Книги** (3-4 книги):
- Название
- Автор
- Краткое описание (2-3 предложения)
- Изображение (можно использовать существующие фото из папки images/)

**Музыкальные треки**:
- Название трека
- Исполнитель
- Аудиофайл (уже есть один файл в папке music/)

**Видео YouTube**:
- 2-3 ссылки на видео с YouTube
- Название каждого видео
- Краткое описание

**Расписание**:
- Дни недели
- Время занятий
- Тип занятия (Hatha, Vinyasa, Yin и т.д.)
- Уровень (Beginner, Intermediate, Advanced)

**Контактная информация**:
- Адрес центра йоги
- Телефон
- Email
- Ссылки на социальные сети и мессенджеры

## Цветовая палитра

**Основные цвета** (теплые, светлые, нежные тона):

- **Основной фон**: `#FFF8F0` (теплый кремовый)
- **Вторичный фон**: `#FFE4D6` (персиковый)
- **Акцентный цвет**: `#D4A574` (золотисто-бежевый)
- **Текст**: `#5D4E37` (теплый коричневый)
- **Ссылки**: `#B8956A` (светло-коричневый)

**Применение через custom.css**:
```css
body {
    background-color: #FFF8F0;
    color: #5D4E37;
}

.w3-theme {
    background-color: #D4A574 !important;
    color: white !important;
}

.w3-theme-light {
    background-color: #FFE4D6 !important;
}

a {
    color: #B8956A;
}
```

## Обработка ошибок

Поскольку сайт статический и не содержит JavaScript, обработка ошибок минимальна:

1. **Отсутствующие изображения**: Браузер отобразит стандартный значок сломанного изображения
2. **Отсутствующие аудиофайлы**: HTML5 audio покажет сообщение "Your browser does not support the audio element"
3. **Проблемы с YouTube**: Если видео недоступно, YouTube iframe покажет соответствующее сообщение
4. **Проблемы с Google Maps**: Если карта не загружается, iframe останется пустым

**Рекомендации**:
- Проверить все пути к файлам перед публикацией
- Убедиться, что все внешние ресурсы (YouTube, Google Maps) доступны
- Использовать атрибут `alt` для всех изображений

## Стратегия тестирования

### Ручное тестирование

**Тест 1: Навигация**
- Открыть каждую страницу
- Проверить, что навигационное меню присутствует
- Кликнуть на каждую ссылку и убедиться, что переход работает

**Тест 2: Контент**
- Проверить, что все изображения загружаются
- Проверить, что аудиоплеер воспроизводит музыку
- Проверить, что видео YouTube загружаются и воспроизводятся
- Проверить, что таблица расписания отображается корректно
- Проверить, что карта Google Maps загружается

**Тест 3: Стилизация**
- Проверить, что W3.CSS подключен (элементы стилизованы)
- Проверить, что custom.css применяется (теплые цвета)
- Проверить, что сайт выглядит согласованно на всех страницах

**Тест 4: Адаптивность**
- Открыть сайт на разных размерах экрана
- Проверить, что W3.CSS классы обеспечивают базовую адаптивность
- Проверить, что контент читаем на мобильных устройствах

**Тест 5: Валидация HTML**
- Использовать W3C HTML Validator для проверки корректности HTML
- Исправить все ошибки валидации

### Браузерная совместимость

Тестировать в следующих браузерах:
- Google Chrome (последняя версия)
- Mozilla Firefox (последняя версия)
- Safari (если доступен)
- Microsoft Edge (последняя версия)

### Чек-лист перед публикацией

- [ ] Все 5 страниц созданы и связаны навигацией
- [ ] Все изображения загружаются
- [ ] Аудиоплеер работает
- [ ] Видео YouTube встроены и воспроизводятся
- [ ] Таблица расписания заполнена
- [ ] Карта Google Maps отображается
- [ ] Контактная информация актуальна
- [ ] W3.CSS подключен через CDN
- [ ] Custom.css применяется
- [ ] HTML валиден (проверено через W3C Validator)
- [ ] Сайт протестирован в основных браузерах
- [ ] Навигация работает на всех страницах

## Дополнительные замечания

### Простота кода

Код должен быть написан так, чтобы студент первого курса мог его понять:

- Использовать простые HTML-теги
- Избегать сложных CSS-селекторов
- Добавлять комментарии к каждой секции
- Использовать понятные имена классов
- Структурировать код с отступами

### Пример комментариев в HTML:

```html
<!-- Навигационное меню -->
<nav class="w3-bar w3-light-grey">
  <!-- Ссылки на страницы -->
  <a href="index.html" class="w3-bar-item w3-button">Home</a>
  ...
</nav>

<!-- Основной контент страницы -->
<main class="w3-container">
  <!-- Секция о преподавателе -->
  <section>
    <h2>About Me</h2>
    ...
  </section>
</main>
```

### Расширяемость

Хотя текущий дизайн простой, он позволяет легко добавлять:
- Больше страниц (просто создать новый HTML-файл и добавить ссылку в навигацию)
- Больше контента (книги, видео, музыка)
- Дополнительные стили через custom.css
- В будущем можно добавить JavaScript для интерактивности (но это не требуется сейчас)
