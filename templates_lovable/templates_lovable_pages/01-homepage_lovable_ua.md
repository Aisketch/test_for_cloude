# Головна сторінка MIDOS - Технічна специфікація

**Тип сторінки:** Landing Page
**URL:** `/` (головна сторінка)  
**Пріоритет:** Критичний
**Підхід:** Mobile First
**Мова:** Українська (UA)
**Останнє оновлення:** 13 листопада 2025

---

## Огляд сторінки

**Призначення:** Головна landing page для представлення платформи MIDOS Digital Twins, демонстрації цінності продукту та залучення до персонального демопоказу.

**Ключові цілі:**
- Передати основну цінність продукту за 3 секунди
- Залучити користувача до бронювання демопоказу  
- Побудувати довіру через компанійну історію та команду
- Навчити про ключові можливості платформи

**Цільові пристрої:**
- Mobile: 320px - 767px (Пріоритет)
- Tablet: 768px - 1023px
- Desktop: 1024px+

---

## Структура сторінки (зверху вниз)

### Блок 01: Header Navigation
**Тип:** Sticky Header  
**Висота Mobile:** 64px
**Висота Desktop:** 80px

#### Mobile Layout (320px - 767px)
```
┌─────────────────────────────────────┐
│ [Логотип]           [☰ Меню]       │
└─────────────────────────────────────┘
```

**Компоненти:**
- **Логотип** (Ліворуч)
  - Розмір: 120px × 32px
  - Посилання: `/`
  - Alt text: "MIDOS - Платформа AI Digital Twins"
  
- **Гамбургер меню** (Праворуч)
  - Іконка: 24px × 24px
  - Колір: Основний текст
  - Відкриває мобільне навігаційне меню

**Мобільне навігаційне меню:**
```
┌─────────────────────────────────────┐
│ [× Закрити]                         │
│                                     │
│ Про нас                             │
│ Блог                                │
│ Документація                        │
│ Контакти                            │
│ ─────────────────                   │
│ [Забронювати демо - CTA]            │
└─────────────────────────────────────┘
```

#### Desktop Layout (1024px+)
```
┌────────────────────────────────────────────────────────────┐
│ [Логотип]    Про нас  Блог  Документація  Контакти  [Забронювати демо] │
└────────────────────────────────────────────────────────────┘
```

**Навігаційні елементи:**
- Про нас → `/about`
- Блог → `/blog`
- Документація → `https://docs.midos.io/`
- Контакти → `/contact`
- Забронювати демо → `/demo` (Primary CTA button)

**Поведінка:**
- Sticky при прокрутці
- Фон: Білий з тінню при прокрутці
- Z-index: 1000

---

### Блок 02: Hero Section
**Висота Mobile:** Auto (min 600px)
**Висота Desktop:** Auto (min 700px)

#### Mobile Layout
```
┌─────────────────────────────────────┐
│                                     │
│         [H1 Заголовок]              │
│                                     │
│      [Підзаголовок]                 │
│                                     │
│   [Primary CTA Button]              │
│   [Secondary CTA Button]            │
│                                     │
│     [Hero Image/Video]              │
│                                     │
└─────────────────────────────────────┘
```

**Контент:**

**H1 Заголовок:**
- Текст: "Особисто з кожним. Одночасно з усіма."
- Розмір шрифту Mobile: 32px / 36px line-height
- Розмір шрифту Desktop: 56px / 64px line-height
- Товщина шрифту: 700
- Колір: Primary text (#0A0A0A)
- Max-width: 600px mobile, 800px desktop
- Вирівнювання: По центру

**Підзаголовок:**
- Текст: "Ваш стиль. Ваша мудрість. Ваш унікальний підхід. Тепер доступний кожному, хто вас потребує. Цілодобово. Віч-на-віч."
- Розмір шрифту Mobile: 16px / 24px line-height
- Розмір шрифту Desktop: 20px / 30px line-height
- Товщина шрифту: 400
- Колір: Secondary text (#666666)
- Max-width: 500px mobile, 640px desktop
- Margin-top: 16px mobile, 24px desktop

**Primary CTA:**
- Текст: "Забронювати персональний показ"
- URL: `/demo`
- Розмір Mobile: Full width (з 20px margin), Висота 56px
- Розмір Desktop: Auto width (padding 24px 48px), Висота 56px
- Розмір шрифту: 16px
- Товщина шрифту: 600
- Фон: Primary color (#0066FF)
- Колір тексту: White
- Border-radius: 8px
- Margin-top: 32px

**Secondary CTA:**
- Текст: "Подивитись демо"
- URL: `#demo-video` or modal trigger
- Розмір Mobile: Full width (з 20px margin), Висота 56px
- Розмір Desktop: Auto width (padding 24px 48px), Висота 56px
- Розмір шрифту: 16px
- Товщина шрифту: 600
- Фон: Transparent
- Колір тексту: Primary color (#0066FF)
- Border: 2px solid primary color
- Border-radius: 8px
- Margin-top: 12px

**Hero Visual:**
- Тип: Image або Looping video
- Mobile: Full width, 300px висота
- Desktop: 600px ширина, 450px висота
- Alt text: "MIDOS Digital Twins - інтерфейс платформи"
- Margin-top: 40px
- Border-radius: 12px
- Опціонально: Легка тінь

**Зображення:**
```markdown
![MIDOS Platform Interface](./assets/images/[SCREENSHOT_HERO_PLATFORM].png)
<!-- IMAGE_REQUIRED: Hero screenshot showing MIDOS platform interface with digital twin conversation -->
```

#### Desktop Layout
```
┌───────────────────────────────────────────────────────────┐
│                                                           │
│   ┌─────────────────────┐     ┌──────────────────────┐  │
│   │                     │     │                      │  │
│   │   [H1 Заголовок]    │     │    [Hero Visual]     │  │
│   │                     │     │                      │  │
│   │ [Підзаголовок]      │     │    Image/Video       │  │
│   │                     │     │                      │  │
│   │ [CTA Buttons Row]   │     │                      │  │
│   │                     │     │                      │  │
│   └─────────────────────┘     └──────────────────────┘  │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

**Desktop Специфіка:**
- Layout з двома колонками: 50/50 split
- Текстова колонка: Ліворуч
- Візуальна колонка: Праворуч
- Max-width container: 1200px
- Padding: 80px 40px

---

### Блок 03: Features Overview - 3 Ключові можливості
**Mobile:** Вертикальний стек
**Desktop:** 3-колонкова сітка

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│         [Eyebrow text]              │
│      [H2 Section Title]             │
│     [Section Description]           │
│                                     │
└─────────────────────────────────────┘
```

**Контент:**
- Eyebrow: "Чому MIDOS"
- Розмір шрифту: 14px, uppercase, letter-spacing: 1.5px
- Колір: Primary brand color (#0066FF)
- Товщина шрифту: 600

- H2: "Ваш AI-близнюк. Ваш спосіб."
- Розмір шрифту Mobile: 28px / 34px line-height
- Розмір шрифту Desktop: 40px / 48px line-height
- Товщина шрифту: 700

- Опис: "Створіть персоналізованого цифрового близнюка, який зберігає ваші знання, особистість та стиль комунікації."
- Розмір шрифту: 16px / 24px line-height
- Колір: Secondary text
- Max-width: 640px
- Margin: 0 auto

**Spacing:**
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px

#### Feature Cards

**Mobile Layout (Стек):**
```
┌─────────────────────────────────────┐
│         [Icon 64×64]                │
│                                     │
│      [Feature Title]                │
│                                     │
│   [Feature description text]        │
│                                     │
└─────────────────────────────────────┘
[Gap: 32px]
┌─────────────────────────────────────┐
│         [Icon 64×64]                │
│      [Feature Title]                │
│   [Feature description]             │
└─────────────────────────────────────┘
```

**Desktop Layout:**
```
┌──────────┬──────────┬──────────┐
│ [Icon]   │ [Icon]   │ [Icon]   │
│ [Title]  │ [Title]  │ [Title]  │
│ [Desc]   │ [Desc]   │ [Desc]   │
└──────────┴──────────┴──────────┘
```

**Feature 1: AI-близнюк з вашими знаннями**
- Icon: AI/Brain icon
- Заголовок: "Ваш AI-близнюк, знає все, що і ви"
- Опис: "Відповідає на 100+ запитів щодня. Вашим голосом. З вашою експертизою. Поки ви робите те, що любите."

**Feature 2: Безмежна кількість розмов**
- Icon: Network/Scale icon
- Заголовок: "Безмежна кількість особистих розмов одночасно"
- Опис: "Кожен клієнт отримує персональну увагу та індивідуальний підхід. Незалежно від того, їх 10 чи 10,000."

**Feature 3: Працює 24/7**
- Icon: Clock/24-7 icon
- Заголовок: "Працює 24/7, поки ви живете своїм життям"
- Опис: "Ваш цифровий близнюк не спить, не їсть, не бере вихідні. Він завжди на зв'язку. Ви повертаєте собі 20+ годин щотижня. Для творчості. Для сім'ї. Для себе."

**Card Styling:**
- Фон: White або light grey (#F9FAFB)
- Padding Mobile: 24px
- Padding Desktop: 32px
- Border-radius: 12px
- Border: 1px solid #E5E7EB (опціонально)
- Hover effect: Легке підняття + тінь (desktop)

**Icon:**
- Розмір: 48px × 48px mobile, 64px × 64px desktop
- Стиль: Outlined або filled
- Колір: Primary brand color (#0066FF)

**Title:**
- Розмір шрифту: 20px / 24px line-height
- Товщина шрифту: 600
- Margin-top: 16px

**Description:**
- Розмір шрифту: 15px / 22px line-height
- Колір: Secondary text
- Margin-top: 8px

**Grid:**
- Mobile: 1 колонка, gap 32px
- Tablet: 2 колонки, gap 24px
- Desktop: 3 колонки, gap 32px

---


### Блок 04: Як це працює
**Призначення:** Показати простий 3-крокови й процес

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│      [H2: "Як це працює"]           │
│   [Підзаголовок]                    │
│                                     │
└─────────────────────────────────────┘
```

**Контент H2:** "Як це працює"
**Підзаголовок:** "Три прості кроки до вашого цифрового близнюка"

**Mobile Layout (Вертикальний таймлайн):**
```
┌─────────────────────────────────────┐
│  ①  [Номер кроку]                   │
│                                     │
│  [Назва кроку]                      │
│  [Опис кроку]                       │
│                                     │
│  [Ілюстрація/Screenshot]            │
│                                     │
│         ↓                           │
│                                     │
│  ②  [Крок 2...]                     │
│                                     │
│         ↓                           │
│                                     │
│  ③  [Крок 3...]                     │
│                                     │
└─────────────────────────────────────┘
```

**Кроки:**

**Крок 1: Створіть свого близнюка**
- Badge: "01"
- Заголовок: "Створіть свого близнюка"
- Опис: "Завантажте свій контент або пройдіть MIDOS Інтерв'ю. Наш AI вивчає ваші знання, тон та особистість за лічені хвилини."
- Зображення: `[SCREENSHOT_STEP_1_BUILD]`
<!-- IMAGE_REQUIRED: Screenshot of content upload interface -->

**Крок 2: Налаштуйте під себе**
- Badge: "02"
- Заголовок: "Налаштуйте під себе"
- Опис: "Точно налаштуйте стиль відповідей, особистісні риси та манеру спілкування. Зробіть його справді вашим за допомогою розширених налаштувань."
- Зображення: `[SCREENSHOT_STEP_2_CUSTOMIZE]`
<!-- IMAGE_REQUIRED: Screenshot of customization dashboard -->

**Крок 3: Запустіть і масштабуйте**
- Badge: "03"  
- Заголовок: "Запустіть і масштабуйте"
- Опис: "Розгорніть свого AI-близнюка на всіх платформах. Спілкуйтеся з вашою аудиторією 24/7, поки ви зосередж єтесь на високоцінній роботі."
- Зображення: `[SCREENSHOT_STEP_3_LAUNCH]`
<!-- IMAGE_REQUIRED: Screenshot of deployment options -->

**Step Badge:**
- Розмір: 48px × 48px
- Фон: Primary color з 10% opacity
- Border: 2px solid primary color
- Розмір шрифту: 20px
- Товщина шрифту: 700
- Border-radius: 50%
- Колір: Primary color (#0066FF)

**Desktop Layout:**
- Чергування ліво-право layout
- Крок 1: Контент ліворуч, зображення праворуч
- Крок 2: Зображення ліворуч, контент праворуч  
- Крок 3: Контент ліворуч, зображення праворуч
- Max-width: 1100px

**Spacing:**
- Section padding Mobile: 60px 20px
- Section padding Desktop: 100px 40px
- Gap між кроками: 48px mobile, 80px desktop

---

### Блок 05: Історія компанії (замість Featured Digital Minds)

**Призначення:** Поділитися історією створення MIDOS та побудувати емоційний зв'язок

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Як все почалося"]            │
│  [Підзаголовок]                     │
│                                     │
└─────────────────────────────────────┘
```

**Контент:**
- H2: "Як все почалося"
- Підзаголовок: "Історія однієї безсонної ночі, яка змінила все"

**Story Content:**

**Момент прозріння**
```
┌─────────────────────────────────────┐
│                                     │
│  📅 1 червня 2025, 2:47 ранку       │
│                                     │
│  Юрій Бог сидів за кухонним столом, │
│  відповідаючи на повторювані        │
│  клієнтські email'и про             │
│  маркетингове позиціонування.       │
│                                     │
│  Замість сну, він зібрав десятиліття│
│  професійних знань — сотні нотаток  │
│  і тисячі слів — в один документ    │
│  і завантажив в AI.                 │
│                                     │
│  Коли він запитав: "Як побудувати   │
│  маркетингову стратегію для         │
│  психолога?" — AI відповів з        │
│  вражаючою ясністю: "його слова.    │
│  Його структура мислення. Його      │
│  приклади".                         │
│                                     │
│  Це одкровення викликало ключове    │
│  питання: Що якщо кожен експерт може│
│  перенести свої знання в цифрову    │
│  версію, здатну обслуговувати тисячі│
│  одночасно?                         │
│                                     │
└─────────────────────────────────────┘
```

**Наша місія**
- Заголовок: "Наша місія"
- Текст: "Звільнити від повторень. Масштабувати вплив. Жити життя."
- Розширений опис: "Ми не продаємо технологію. Ми повертаємо експертам право на власне життя. Більше успішних експертів означає більше ув'язнення у власному успіху. Більше клієнтів = менше часу на кожного. Більше питань = більше повторень. Більше впливу = більше вигорання. MIDOS розриває це коло."

**Наше бачення**
- Заголовок: "Наше бачення"  
- Текст: "Ваш AI-близнюк працює в цифрі, а ви живете в реальності."
- Розширений опис: "Світ, де цифрове і реальне природно розділені. Ваш AI-близнюк працює 24/7 — відповідає на email'и о 3 ранку, проводить консультації через часові пояси, обробляє сотні запитів одночасно. А ви живете реальним життям — сім'я без телефонів, стратегічна творча робота, справжня присутність."

**Styling:**
- Фон: Light grey (#F9FAFB) або gradient
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px
- Max-width text: 700px centered

---

### Блок 06: Testimonials  
**Статус:** ПРОПУЩЕНО - немає реальних відгуків (MVP стадія)

```markdown
<!-- BLOCK_SKIPPED: Testimonials -->
<!-- REASON: MVP stage - no real customer testimonials yet -->
<!-- TODO: Add testimonials after first 10 customers -->
```

---

### Блок 07: Use Cases або Команда
**Призначення:** Показати команду засновників

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Команда, яка це створила"]   │
│  [Підзаголовок]                     │
│                                     │
└─────────────────────────────────────┘
```

**Контент:**
- H2: "Команда, яка це створила"
- Підзаголовок: "Три засновники з досвідом у маркетингу, операціях та технологіях"

**Team Grid (3 колонки Desktop, стек Mobile):**

**Член команди 1:**
```
┌──────────────────────┐
│                      │
│   [Фото 3:4]         │
│                      │
│   Юрій Бог           │
│   CEO & Co-Founder   │
│                      │
│   Старший по         │
│   маркетингу         │
│                      │
└──────────────────────┘
```
- Ім'я: Юрій Бог
- Посада: CEO & Co-Founder
- Роль: Старший по маркетингу
- Фото: `[TEAM_PHOTO_YURIY_BOH]`
<!-- IMAGE_REQUIRED: Professional photo of Yuriy Boh, format 3:4 -->

**Член команди 2:**
- Ім'я: Яна Барко
- Посада: COO & Co-Founder
- Роль: Старша по порядку
- Фото: `[TEAM_PHOTO_YANA_BARKO]`
<!-- IMAGE_REQUIRED: Professional photo of Yana Barko, format 3:4 -->

**Член команди 3:**
- Ім'я: Дмитро Загорулько
- Посада: CTO & Co-Founder
- Роль: Старший по технічній частині
- Фото: `[TEAM_PHOTO_DMYTRO_ZAHORULKO]`
<!-- IMAGE_REQUIRED: Professional photo of Dmytro Zahorulko, format 3:4 -->

**Card Styling:**
- Розмір фото: Повна ширина картки, співвідношення 3:4
- Border-radius: 12px
- Padding: 24px
- Background: White
- Border: 1px solid #E5E7EB

**Name:**
- Розмір шрифту: 20px
- Товщина шрифту: 600
- Margin-top: 16px

**Title:**
- Розмір шрифту: 14px
- Колір: Primary brand color (#0066FF)
- Margin-top: 4px

**Role:**
- Розмір шрифту: 15px / 22px line-height
- Колір: Secondary text
- Margin-top: 12px

---

### Блок 08: Demo Booking (замість Pricing Teaser)
**Призначення:** Залучити до бронювання персонального показу

```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Готові побачити MIDOS        │
│        в дії?"]                     │
│  [Підзаголовок]                     │
│                                     │
│  ┌──────────────────────────────┐  │
│  │                              │  │
│  │   [Demo Booking Card]        │  │
│  │                              │  │
│  │   • Персональний показ 1:1   │  │
│  │   • 30 хвилин з експертом    │  │
│  │   • Відповіді на всі питання │  │
│  │   • Індивідуальна ціна       │  │
│  │                              │  │
│  │   [Забронювати демо]         │  │
│  │                              │  │
│  └──────────────────────────────┘  │
│                                     │
└─────────────────────────────────────┘
```

**Контент:**
- H2: "Готові побачити MIDOS в дії?"
- Підзаголовок: "Забронюйте персональний показ з нашою командою. Покажемо, як MIDOS може змінити ваш бізнес."

**Demo Card:**
- Заголовок: "Персональний демопоказ"
- Список переваг:
  - ✓ Показ платформи 1:1
  - ✓ 30 хвилин з експертом
  - ✓ Відповіді на всі ваші питання
  - ✓ Індивідуальне ціноутворення
  - ✓ Без зобов'язань

**CTA Button:**
- Текст: "Забронювати персональний показ"
- URL: `/demo`
- Стиль: Primary button (повна ширина на mobile)
- Розмір: Height 56px
- Фон: Primary color (#0066FF)

**Альтернативне посилання:**
- Текст: "Або напишіть нам → hello@midos.io"
- Розмір шрифту: 14px
- Колір: Secondary text
- Margin-top: 16px

---

### Блок 09: Final CTA Section
**Призначення:** Остання можливість для конверсії

**Фон:** Gradient (Primary to Secondary brand color)

```
┌─────────────────────────────────────┐
│                                     │
│     [H2: Сильний CTA заголовок]     │
│                                     │
│     [Текст підтримки]               │
│                                     │
│     [Primary CTA Button]            │
│     [Secondary text link]           │
│                                     │
└─────────────────────────────────────┘
```

**Контент:**
- H2: "Готові повернути собі життя?"
- Розмір шрифту Mobile: 28px / 34px line-height
- Розмір шрифту Desktop: 40px / 48px line-height
- Колір: White (темний фон)
- Вирівнювання: По центру

- Підтекст: "Приєднуйтесь до експертів, які використовують MIDOS для масштабування свого впливу. Почніть з персонального показу."
- Розмір шрифту: 18px / 26px line-height
- Колір: White з 90% opacity
- Margin-top: 16px

- Primary CTA: "Забронювати персональний показ"
- URL: `/demo`
- Розмір Mobile: Full width (max 400px)
- Розмір Desktop: Auto width (padding 24px 64px)
- Висота: 56px
- Фон: White
- Колір тексту: Primary brand color (#0066FF)
- Розмір шрифту: 16px
- Товщина шрифту: 600
- Margin-top: 32px

- Secondary link: "Подивитись відео-демо"
- Розмір шрифту: 16px
- Колір: White
- Text decoration: Underline
- Margin-top: 16px

**Section Styling:**
- Фон: Linear gradient (#0066FF to #7928CA)
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px
- Вирівнювання: По центру

---


### Блок 10: Footer
**Тип:** Multi-column footer

#### Mobile Layout (Стековані секції)
```
┌─────────────────────────────────────┐
│  [Логотип]                          │
│  [Тагл айн]                         │
│                                     │
│  Продукт                            │
│  - Документація                     │
│  - Блог                             │
│                                     │
│  Компанія                           │
│  - Про нас                          │
│  - Команда                          │
│  - Контакти                         │
│                                     │
│  [Social Icons]                     │
│  [LinkedIn] [Instagram] [X]         │
│  [Facebook] [YouTube] [TikTok]      │
│  [Telegram]                         │
│                                     │
│  ─────────────────────              │
│                                     │
│  © 2025 MIDOS.IO.                   │
│  Всі права захищені.                │
│                                     │
│  Україна, м. Київ, Шевченка 23      │
│                                     │
└─────────────────────────────────────┘
```

#### Desktop Layout (Multi-column)
```
┌───────────────────────────────────────────────────────────┐
│                                                           │
│  [Логотип]           Продукт      Компанія               │
│  [Тагляйн]           - Документація - Про нас            │
│                      - Блог        - Команда             │
│  [Social Icons]                    - Контакти            │
│                                                           │
│  ─────────────────────────────────────────────────────   │
│                                                           │
│  © 2025 MIDOS.IO. Всі права захищені.  [Social Icons]    │
│  Україна, м. Київ, Шевченка 23                           │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

**Logo Section:**
- Логотип: 140px × 36px
- Тагляйн: "Особисто з кожним. Одночасно з усіма."
- Розмір шрифту: 14px
- Колір: Secondary text (#6B7280)
- Max-width: 280px
- Margin-top: 12px

**Footer Columns:**

**Колонка 1: Продукт**
- Документація → `https://docs.midos.io/`
- Блог → `/blog`

**Колонка 2: Компанія**
- Про нас → `/about`
- Команда → `/about#team`
- Контакти → `/contact`

**Column Heading:**
- Розмір шрифту: 14px
- Товщина шрифту: 600
- Колір: Primary text
- Margin-bottom: 12px
- Text transform: Uppercase
- Letter spacing: 0.5px

**Footer Links:**
- Розмір шрифту: 14px
- Колір: Secondary text (#6B7280)
- Line-height: 32px
- Hover: Primary color (#0066FF)

**Social Icons:**
- Розмір: 24px × 24px
- Колір: Secondary text
- Hover: Primary color
- Gap: 16px
- Display: Flex row

**Social Links:**
- LinkedIn → `https://www.linkedin.com/company/midos_io`
- Instagram → `https://www.instagram.com/midos_io`
- X (Twitter) → `https://x.com/midos_io`
- Facebook → `https://www.facebook.com/people/Midos/61581132000448/`
- YouTube → `https://www.youtube.com/@midos_io`
- TikTok → `https://www.tiktok.com/@midos_io`
- Telegram → `https://t.me/midos_io`

**Copyright Bar:**
- Текст: "© 2025 MIDOS.IO. Всі права захищені."
- Адреса: "Україна, м. Київ, вул. Шевченка 23"
- Email: "hello@midos.io"
- Розмір шрифту: 14px
- Колір: Secondary text (#6B7280)
- Padding-top: 24px
- Border-top: 1px solid #E5E7EB

**Footer Styling:**
- Фон: #F9FAFB або White
- Padding Mobile: 48px 20px 24px
- Padding Desktop: 60px 40px 32px
- Border-top: 1px solid #E5E7EB (опціонально)

**Grid:**
- Mobile: 1 колонка, стек всіх секцій
- Tablet: 2 колонки (Logo + Продукт, Компанія)
- Desktop: 3 колонки (Logo займає 2x ширину, інші 1x)
- Gap: 40px mobile, 60px desktop

---

## Інтерактивні елементи

### 1. Sticky Header
- **Тригер:** При прокрутці > 100px
- **Поведінка:**
  - Додати фоновий колір (білий)
  - Додати тінь: `0 2px 4px rgba(0,0,0,0.08)`
  - Зменшити висоту на 10% (опціонально)
- **Анімація:** Плавний перехід 0.3s

### 2. Мобільна навігація
- **Відкриття:** Slide зправа, 300ms ease-out
- **Overlay:** Темний фон, 40% opacity
- **Закриття:** Клік на overlay або кнопку закриття
- **Lock scroll:** Коли меню відкрите

### 3. Scroll Animations
- **Fade in:** Елементи з'являються при вході в viewport
- **Slide up:** Елементи піднімаються на 20px при появі
- **Stagger:** Послідовна анімація для груп (50ms затримка)
- **Тригер:** IntersectionObserver, threshold 0.2

### 4. Button States
- **Default:** Primary color фон
- **Hover:** Затемнення на 10%, підняття на 2px (desktop)
- **Active:** Scale 0.98
- **Focus:** Outline 2px primary color
- **Disabled:** 50% opacity, cursor not-allowed

### 5. Card Hover Effects (Desktop)
- **Default:** Тінь: `0 1px 3px rgba(0,0,0,0.1)`
- **Hover:**
  - Lift: `translateY(-4px)`
  - Тінь: `0 8px 16px rgba(0,0,0,0.15)`
  - Transition: 0.3s ease

---

## Оптимізація продуктивності

### Зображення
- **Формат:** WebP з JPG fallback
- **Lazy loading:** Всі зображення нижче fold
- **Responsive:** srcset для різних розмірів екрану
- **Compression:** 80% якість
- **Розміри:** Відповідні розміри для breakpoint'ів

### Hero Video (якщо застосовується)
- **Формат:** MP4 (H.264)
- **Розмір:** Max 5MB
- **Розміри:** 1920×1080 max
- **Autoplay:** Muted, loop, без контролів
- **Fallback:** Статичне зображення для mobile

### Fonts
- **Loading:** font-display: swap
- **Subset:** Кирилиця + Latin
- **Formats:** WOFF2 primary, WOFF fallback
- **Preload:** Тільки критичні шрифти

### JavaScript
- **Loading:** Defer для некритичних скриптів
- **Bundling:** Code splitting по route
- **Minification:** Production builds
- **Caching:** Агресивні cache headers

### CSS
- **Critical CSS:** Inline above-fold стилі
- **Loading:** Defer некритичних stylesheets
- **Minification:** Видалення пробілів, коментарів
- **Purge:** Видалення невикористаних стилів

---

## Вимоги доступності

### Semantic HTML
- Використовувати відповідну ієрархію заголовків (H1 → H2 → H3)
- Використовувати `<nav>`, `<main>`, `<section>`, `<article>` landmarks
- Використовувати `<button>` для інтерактивних елементів, не `<div>`

### ARIA Labels
- Navigation: `aria-label="Головна навігація"`
- Hamburger: `aria-label="Відкрити меню"` + `aria-expanded`
- Buttons: Описові `aria-label` коли текст не зрозумілий

### Клавіатурна навігація
- Всі інтерактивні елементи мають бути focusable
- Tab порядок має бути логічним
- Focus індикатори мають бути видимі (outline)
- Escape key закриває модали/меню

### Screen Readers
- Зображення: Описові alt тексти
- Іконки: `aria-label` або `aria-hidden="true"` якщо декоративні
- Посилання: Чіткі цілі, уникати "клікніть тут"
- Form inputs: Пов'язані labels

### Колірний контраст
- Текст на фонах: WCAG AA мінімум (4.5:1)
- Великий текст (18px+): 3:1 мінімум
- Інтерактивні елементи: 3:1 проти фону

---

## Responsive Breakpoints

```css
/* Mobile First Approach */

/* Mobile Small: 320px - 374px */
@media (min-width: 320px) { }

/* Mobile Medium: 375px - 424px */
@media (min-width: 375px) { }

/* Mobile Large: 425px - 767px */
@media (min-width: 425px) { }

/* Tablet: 768px - 1023px */
@media (min-width: 768px) { }

/* Desktop: 1024px - 1439px */
@media (min-width: 1024px) { }

/* Desktop Large: 1440px+ */
@media (min-width: 1440px) { }
```

**Container Max-widths:**
- Mobile: 100% (з 20px padding)
- Tablet: 720px
- Desktop: 1100px
- Desktop Large: 1200px

---

## Design Tokens

### Кольори
```
Primary Brand: #0066FF (Vibrant Blue)
Primary Hover: #0052CC
Secondary Brand: #7928CA (Transformational Purple)
Tertiary Brand: #3D25D3 (Deep Indigo)

Primary Text: #0A0A0A (Near Black)
Secondary Text: #6B7280 (Grey)
Tertiary Text: #9CA3AF (Light Grey)

Background Primary: #FFFFFF (White)
Background Secondary: #F9FAFB (Light Grey)
Background Accent: #EEF2FF (Light Blue)

Border Default: #E5E7EB (Light Grey)
Border Focus: #0066FF (Primary)

Success: #10B981 (Green)
Warning: #F59E0B (Orange)
Error: #EF4444 (Red)
Info: #3B82F6 (Blue)
```

### Типографія
```
Font Family:
  - Primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif
  - Headings: 'Alegreya Sans', sans-serif
  - Mono: 'Roboto Mono', 'Courier New', monospace

Font Sizes (Mobile / Desktop):
  - H1: 32px / 56px
  - H2: 28px / 40px
  - H3: 24px / 32px
  - H4: 20px / 24px
  - Body: 16px / 16px
  - Small: 14px / 14px
  - Tiny: 12px / 12px

Font Weights:
  - Regular: 400
  - Medium: 500
  - Semibold: 600
  - Bold: 700

Line Heights:
  - Tight: 1.2
  - Normal: 1.5
  - Relaxed: 1.75
```

### Spacing Scale
```
xs: 4px
sm: 8px
md: 16px
lg: 24px
xl: 32px
2xl: 40px
3xl: 48px
4xl: 64px
5xl: 80px
6xl: 100px
```

### Border Radius
```
sm: 4px
md: 8px
lg: 12px
xl: 16px
2xl: 24px
full: 9999px (кола)
```

### Shadows
```
sm: 0 1px 2px rgba(0,0,0,0.05)
md: 0 4px 6px rgba(0,0,0,0.1)
lg: 0 10px 15px rgba(0,0,0,0.1)
xl: 0 20px 25px rgba(0,0,0,0.15)
```

---

## Animation Timing
```
Fast: 150ms
Normal: 300ms
Slow: 500ms

Easing:
  - ease-out: cubic-bezier(0, 0, 0.2, 1)
  - ease-in: cubic-bezier(0.4, 0, 1, 1)
  - ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)
```

---

## SEO Metadata

### Meta Tags (HTML Head)

#### Українська версія
```html
<!-- Primary Meta Tags -->
<title>MIDOS - Особисто з кожним. Одночасно з усіма. | AI Digital Twins</title>
<meta name="title" content="MIDOS - Особисто з кожним. Одночасно з усіма." />
<meta name="description" content="Створіть свого AI-близнюка, який працює 24/7. Масштабуйте вашу експертизу без вигорання. Повертаєте собі 20+ годин щотижня." />
<meta name="keywords" content="AI близнюк, цифровий близнюк, штучний інтелект, автоматизація, масштабування бізнесу" />
<meta name="theme-color" content="#0066FF" />
<meta name="robots" content="index, follow" />
<link rel="canonical" href="https://midos.io/" />

<!-- Open Graph / Facebook -->
<meta property="og:type" content="website" />
<meta property="og:url" content="https://midos.io/" />
<meta property="og:title" content="MIDOS - Особисто з кожним. Одночасно з усіма." />
<meta property="og:description" content="Створіть свого AI-близнюка, який працює 24/7. Масштабуйте вашу експертизу без вигорання." />
<meta property="og:image" content="https://midos.io/images/og-image-ua.png" />
<meta property="og:locale" content="uk_UA" />
<meta property="og:locale:alternate" content="en_US" />

<!-- Twitter -->
<meta property="twitter:card" content="summary_large_image" />
<meta property="twitter:url" content="https://midos.io/" />
<meta property="twitter:title" content="MIDOS - Особисто з кожним. Одночасно з усіма." />
<meta property="twitter:description" content="Створіть свого AI-близнюка, який працює 24/7." />
<meta property="twitter:image" content="https://midos.io/images/twitter-image-ua.png" />

<!-- Favicon -->
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png" />
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
```

### Structured Data (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "MIDOS",
  "legalName": "MIDOS.IO",
  "url": "https://midos.io",
  "logo": "https://midos.io/logo.png",
  "foundingDate": "2025-09-07",
  "founders": [
    {
      "@type": "Person",
      "name": "Юрій Бог"
    },
    {
      "@type": "Person",
      "name": "Яна Барко"
    },
    {
      "@type": "Person",
      "name": "Дмитро Загорулько"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "вул. Шевченка 23",
    "addressLocality": "Київ",
    "addressCountry": "UA"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "",
    "contactType": "Customer Service",
    "email": "hello@midos.io",
    "availableLanguage": ["Ukrainian", "English"]
  },
  "sameAs": [
    "https://www.linkedin.com/company/midos_io",
    "https://www.instagram.com/midos_io",
    "https://x.com/midos_io",
    "https://www.facebook.com/people/Midos/61581132000448/",
    "https://www.youtube.com/@midos_io",
    "https://www.tiktok.com/@midos_io",
    "https://t.me/midos_io"
  ]
}
```

---

## Контрольний список тестування

### Функціональне тестування
- [ ] Всі посилання ведуть на правильні URL
- [ ] Всі кнопки тригерують правильні дії
- [ ] Навігаційне меню відкривається/закривається коректно
- [ ] CTA кнопки клікабельні та ведуть на правильні сторінки

### Responsive тестування
- [ ] Тест на iPhone SE (320px)
- [ ] Тест на iPhone 12/13 (390px)
- [ ] Тест на iPad (768px)
- [ ] Тест на Desktop (1280px, 1920px)
- [ ] Тест landscape орієнтації на mobile/tablet
- [ ] Перевірка що текст не виходить за межі контейнерів
- [ ] Зображення масштабуються правильно без спотворень

### Браузерне тестування
- [ ] Chrome (останній)
- [ ] Firefox (останній)
- [ ] Safari (останній)
- [ ] Edge (останній)
- [ ] Mobile Safari (iOS)
- [ ] Chrome Mobile (Android)

### Тестування продуктивності
- [ ] Lighthouse score > 90
- [ ] First Contentful Paint < 1.5s
- [ ] Largest Contentful Paint < 2.5s
- [ ] Загальна вага сторінки < 2MB
- [ ] Зображення оптимізовані (WebP)
- [ ] Шрифти завантажуються ефективно

### Тестування доступності
- [ ] Клавіатурна навігація працює
- [ ] Screen reader протестовано (NVDA/VoiceOver)
- [ ] Колірний контраст проходить WCAG AA
- [ ] Focus індикатори видимі
- [ ] ARIA labels присутні де потрібно
- [ ] Використано Semantic HTML
- [ ] Alt текст на всіх зображеннях

---

## Примітки для розробників

### Tech Stack Рекомендації
- **Framework:** React, Next.js, або Nuxt
- **Styling:** Tailwind CSS або CSS Modules
- **Animations:** Framer Motion або GSAP
- **Forms:** React Hook Form + Zod validation

### Пріоритети завантаження сторінки
1. **Критично:** Header, Hero section, fonts
2. **Високо:** Features, How It Works
3. **Середньо:** Company Story, Team
4. **Низько:** Footer

---

## Історія версій

**v1.0** - 13 листопада 2025
- Початкова специфікація головної сторінки MIDOS (українська версія)
- Mobile-first підхід
- Повна деталізація блоків від header до footer
- Адаптація під MVP стадію (без testimonials, з demo booking замість pricing)

---

**Кінець специфікації головної сторінки MIDOS (UA)**

