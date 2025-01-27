# Лекція 4: Вступ до Bootstrap

## Що таке Bootstrap?

### Теорія:
- Bootstrap — це популярний CSS-фреймворк для створення адаптивних і привабливих сайтів.
- Переваги:
  - Готові компоненти: кнопки, форми, меню, модальні вікна.
  - Простота у використанні.
  - Адаптивний дизайн за замовчуванням.
  - Включає в себе CSS і JavaScript.

## Підключення Bootstrap

### Дія:
- Пояснюємо, як підключити Bootstrap через CDN:
  1. Відкриваємо офіційний сайт Bootstrap.
  2. Копіюємо лінки для підключення CSS і JS.
  3. Додаємо їх у `<head>` і перед закриваючим тегом `<body>`:
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

### Теорія:
- CDN (Content Delivery Network) — це спосіб завантаження фреймворку без необхідності завантажувати файли локально.
- Bootstrap автоматично додає стилі для елементів HTML.

## Використання готового шаблону

### Дія:
- Переходимо на сторінку готових шаблонів на Bootstrap Examples.
- Вибираємо простий шаблон, наприклад, “Starter template”.
- Скопіюємо код і пояснюємо, як він працює:
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap Starter</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  </head>
  <body>
    <header>
      <nav class="navbar navbar-expand-md navbar-dark bg-dark">
        <div class="container-fluid">
          <a class="navbar-brand" href="#">MySite</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
              <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
              <li class="nav-item"><a class="nav-link" href="#">About</a></li>
              <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
    <main class="container">
      <div class="py-5">
        <h1>Welcome to Bootstrap</h1>
        <p>This is a simple starter template.</p>
      </div>
    </main>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```

## Огляд компонентів Bootstrap

### Дія:
- Демонструємо кілька компонентів:
  - Кнопка:
```html
<button class="btn btn-primary">Primary Button</button>
```
  - Адаптивний грід:
```html
<div class="container">
  <div class="row">
    <div class="col-4">Column 1</div>
    <div class="col-4">Column 2</div>
    <div class="col-4">Column 3</div>
  </div>
</div>
```
  - Карточка:
```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card Title</h5>
    <p class="card-text">Some quick example text.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```

## Детальне пояснення основних концепцій Bootstrap

### Сіткова система Bootstrap

#### Теорія:
- Сіткова система Bootstrap базується на гнучких контейнерах, рядках і колонках.
- Контейнери (`.container` або `.container-fluid`) використовуються для вирівнювання контенту.
- Рядки (`.row`) використовуються для створення горизонтальних груп колонок.
- Колонки (`.col-`) використовуються для створення вертикальних груп контенту.

#### Приклад:
```html
<div class="container">
  <div class="row">
    <div class="col-md-4">Колонка 1</div>
    <div class="col-md-4">Колонка 2</div>
    <div class="col-md-4">Колонка 3</div>
  </div>
</div>
```

### Утилітарні класи Bootstrap

#### Теорія:
- Утилітарні класи Bootstrap дозволяють швидко застосовувати стилі до елементів без написання додаткового CSS.
- Вони включають класи для відступів, вирівнювання, кольорів, розмірів та інших властивостей.

#### Приклад:
```html
<div class="p-3 mb-2 bg-primary text-white">Primary Background</div>
<div class="text-center">Центрований текст</div>
<div class="d-flex justify-content-between">
  <div>Елемент 1</div>
  <div>Елемент 2</div>
</div>
```

### Принципи адаптивного дизайну Bootstrap

#### Теорія:
- Bootstrap використовує медіазапити для створення адаптивного дизайну.
- Класи Bootstrap автоматично адаптуються до різних розмірів екранів.
- Використання класів, таких як `.d-none`, `.d-sm-block`, `.d-md-none`, дозволяє контролювати видимість елементів на різних пристроях.

#### Приклад:
```html
<div class="d-none d-md-block">Видимий тільки на середніх і великих екранах</div>
<div class="d-block d-sm-none">Видимий тільки на маленьких екранах</div>
```

## Завершення

### Теорія:
- Bootstrap дозволяє швидко створювати професійні сайти.
- Його компоненти можна кастомізувати, щоб відповідати вашим вимогам.
