# Лекція 3: Адаптивність, Flexbox і Position

## Що таке адаптивність?

### Теорія:
- Адаптивність — це здатність сайту змінювати свій вигляд залежно від розміру екрана.
- Використовується для покращення зручності користування на різних пристроях.

### Дія:
- Створюємо медіазапит у styles.css:
```css
@media (max-width: 768px) {
    .students-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    .menu {
        flex-direction: column;
        align-items: center;
    }
}
@media (max-width: 480px) {
    .students-grid {
        grid-template-columns: 1fr;
    }
    .student {
        width: 100%;
        max-width: 300px;
    }
}
```

### Теорія:
- `@media` — це CSS-директива для визначення умов, коли стилі мають застосовуватися.
- `max-width` визначає максимальну ширину екрану.
- У цьому прикладі:
  - При ширині екрана менше 768px змінюємо структуру гріда і орієнтацію меню.
  - При ширині менше 480px — студенти займають 100% ширини.

## Властивість display

### Теорія:
- `display` визначає, як елементи розташовуються на сторінці.
- Основні значення:
  - `block` — елемент займає весь доступний простір по ширині.
  - `inline` — елемент розташовується в ряд.
  - `flex` — елемент стає частиною гнучкого контейнера.
  - `grid` — елемент стає частиною грід-контейнера.

### Дія:
- Перетворюємо блок студентів на Flex-контейнер:
```css
.students-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    gap: 20px;
}
```

### Теорія:
- `flex-wrap: wrap` дозволяє елементам переноситися на новий ряд.
- `justify-content: space-around` додає рівномірні відступи між елементами.

## Flexbox для меню

### Дія:
- Змінюємо меню на Flexbox:
```css
.menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

### Теорія:
- Flexbox дозволяє вирівнювати елементи горизонтально або вертикально.
- `justify-content: space-between` — елементи рівномірно розташовані з проміжками.
- `align-items: center` — вирівнювання по вертикалі.

## Властивість position

### Теорія:
- `position` визначає спосіб розташування елемента:
  - `static` (за замовчуванням) — звичайний потік.
  - `relative` — елемент зміщується відносно свого початкового положення.
  - `absolute` — елемент зміщується відносно найближчого відносного контейнера.
  - `fixed` — елемент закріплюється на екрані, незалежно від прокрутки.

### Дія:
- Додаємо позиціонування до заголовка:
```css
.main-header {
    position: relative;
}
.main-header h1 {
    position: absolute;
    top: 10px;
    left: 20px;
    background-color: rgba(255, 255, 255, 0.8);
    padding: 10px;
    border-radius: 5px;
}
```

### Теорія:
- У цьому прикладі:
  - `relative` задає початкове положення.
  - `absolute` зміщує заголовок усередині контейнера `.main-header`.

## Властивість display:grid

### Теорія:
- `display:grid` дозволяє створювати складні макети за допомогою грід-системи.
- Основні властивості:
  - `grid-template-columns` — визначає кількість і розміри колонок.
  - `grid-template-rows` — визначає кількість і розміри рядків.
  - `gap` — відстань між елементами гріда.

### Дія:
- Створюємо грід-контейнер:
```css
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: auto;
    gap: 20px;
}
.grid-item {
    background-color: #f2f2f2;
    padding: 20px;
    border: 1px solid #ccc;
}
```

### Теорія:
- `repeat(3, 1fr)` створює три колонки однакової ширини.
- `auto` дозволяє рядкам автоматично підлаштовуватися під вміст.
- `gap: 20px` додає відстань між елементами гріда.

## Властивість display:flex

### Теорія:
- `display:flex` дозволяє створювати гнучкі макети за допомогою Flexbox.
- Основні властивості:
  - `flex-direction` — визначає напрямок розташування елементів.
  - `justify-content` — вирівнювання елементів по головній осі.
  - `align-items` — вирівнювання елементів по перпендикулярній осі.

### Дія:
- Створюємо гнучкий контейнер:
```css
.flex-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.flex-item {
    background-color: #f2f2f2;
    padding: 20px;
    border: 1px solid #ccc;
}
```

### Теорія:
- `flex-direction: row` розташовує елементи в ряд.
- `justify-content: space-between` додає рівномірні відступи між елементами.
- `align-items: center` вирівнює елементи по вертикалі.
