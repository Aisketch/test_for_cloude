# MIDOS Platform - Knowledge Base (FILLED)

## 1. БІЗНЕС-КОНТЕКСТ

### 1.1 Проект

- **Назва проекту**: MIDOS.IO
- **Слоган/Tagline**:
  - 🇺🇦 UA: "Особисто з кожним. Одночасно з усіма."
  - 🇬🇧 EN: "One-on-one with everyone, all at the same time."
- **Місія**:
  - 🇺🇦 UA: "Звільнити від повторень. Масштабувати вплив. Жити життя."
  - 🇬🇧 EN: "Free from repetition. Scale impact. Return life."
- **Конкурент для аналізу**: delphi.ai
- **Унікальна пропозиція (USP)**:
  - 🇺🇦 UA: "Ваш стиль. Ваша мудрість. Ваш унікальний підхід. Тепер доступний кожному, хто вас потребує. Цілодобово. Віч-на-віч."
  - 🇬🇧 EN: "Your style. Your wisdom. Your exclusive approach. Now available to everyone who needs you. Around the clock. One-on-one."

### 1.2 Цільова аудиторія

- **Основна ЦА**: Експерти, коучі, консультанти, thought leaders які хочують масштабувати свій вплив та звільнити час від повторюваних завдань
- **Вторинна ЦА**: Бізнес-власники, автори, подкастери, executives які потребують автоматизації комунікацій з клієнтами
- **Pain points**:
  1. Витрачають 20+ годин щотижня на однотипні запитання клієнтів
  2. Не можуть масштабувати особисту експертизу через обмеженість часу
  3. Втрачають потенційних клієнтів через неможливість відповідати 24/7
  4. Вигоряють від повторюваної роботи замість творчої діяльності
- **Jobs to be done**:
  1. Автоматизувати відповіді на повторювані питання клієнтів
  2. Масштабувати експертизу без втрати особистого підходу
  3. Звільнити час для високоцінної роботи та особистого життя
  4. Забезпечити 24/7 доступність для клієнтів

### 1.3 Бізнес-модель

- **Тип**: SaaS (Software as a Service)
- **Монетизація**: Custom pricing після персонального demo call
- **Pricing tiers**: Немає фіксованих тарифів на MVP стадії. Індивідуальне ціноутворення для кожного клієнта після демонстрації.

---

## 2. БРЕНД ТА ВІЗУАЛЬНА ІДЕНТИЧНІСТЬ

### 2.1 Brand Voice & Tone

- **Характер бренду**: Інноваційний, професійний, натхненний, технологічно-передовий, але людяний
- **Tone of voice UA**: Прямий, впевнений, емоційно-резонуючий. Говоримо про свободу та повернення життя, а не про технології
- **Tone of voice EN**: Confident, inspiring, human-centered. Focus on life transformation, not just technology features
- **Заборонені слова/фрази**:
  - Уникати: "штучний інтелект замінює вас", "робот", "автоматизація" (без контексту цінності)
  - Не вживати: технічний жаргон без пояснень
  - Філософія: "Ми не продаємо технологію. Ми повертаємо експертам право на власне життя."

### 2.2 Дизайн-система (Базові значення)

```css
/* КОЛЬОРИ - HSL значення */
--primary: 220 100% 50%;        /* #0066FF - Vibrant Blue */
--primary-foreground: 0 0% 100%; /* White */
--secondary: 269 67% 47%;        /* #7928CA - Transformational Purple */
--accent: 253 78% 52%;           /* #3D25D3 - Deep Indigo */
--background: 0 0% 100%;         /* White */
--foreground: 210 10% 23%;       /* #343a40 - Dark gray for text */
--muted: 210 10% 94%;            /* #f1f1f1 - Light gray */
--border: 210 10% 82%;           /* #6c757d - Medium gray */

/* ГРАДІЄНТИ */
--gradient-primary: linear-gradient(135deg, hsl(269 67% 47%), hsl(253 78% 52%), hsl(220 100% 50%));
--gradient-hero: linear-gradient(135deg, #7928CA 0%, #3D25D3 50%, #0066FF 100%);

/* ТІНІ */
--shadow-elegant: 0 8px 24px rgba(0, 102, 255, 0.12);
--shadow-card: 0 4px 12px rgba(0, 0, 0, 0.08);
```

### 2.3 Типографіка

- **Primary font**: Alegreya Sans (для заголовків та акцентів)
- **Weights used**: 400 (Regular), 600 (Semibold), 700 (Bold)
- **Heading style**: Tight letter spacing для великих заголовків, normal для H3-H6
- **Body style**: Inter, Regular 400, line-height 1.6 для оптимальної читабельності

### 2.4 Анімації та Interaction

- **Animation style**: Subtle (тонкі, професійні анімації без перебільшення)
- **Transition timing**: 0.3s ease-out (для більшості переходів), 0.2s ease для hover
- **Hover effects**: Легке підняття карток (translateY(-4px)), зміна тіні, scale(1.05) для кнопок
- **Scroll animations**: TAK - fade in, slide up для секцій при скролі (використати Intersection Observer)

---

## 3. ТЕХНІЧНИЙ СТЕК ТА АРХІТЕКТУРА

### 3.1 Frontend

- **Framework**: React + Vite + TypeScript ✓
- **Styling**: Tailwind CSS ✓
- **Animations**: GSAP + Three.js ✓
- **Component library**: shadcn/ui + 21st.dev components ✓
- **State management**: React Query (для server state) + Zustand (для client state)

### 3.2 Backend & Database

- **Backend**: Lovable Cloud (Supabase) ✓
- **Authentication**: Email/Password + OAuth (Google)
- **Database structure**:
  - users (id, email, created_at, updated_at)
  - profiles (user_id, full_name, phone, company, role)
  - demo_requests (id, full_name, email, phone, company, message, source, utm_params, created_at, status)
  - industries (id, slug, name_en, name_ua, description_en, description_ua)
  - blog_posts (id, slug, title_en, title_ua, content_en, content_ua, category, published_at)
  - quiz_responses (id, user_email, answers, score, created_at)

### 3.3 Інтеграції

- **Calendar**: Форма /demo відправляє дані в Zoho CRM (не використовуємо календарну інтеграцію)
- **CRM**: Zoho CRM - всі заявки з форм падають туди
- **Payments**: Не потрібно для MVP
- **Email**: Supabase Auth для автентифікації, Resend для маркетингових email (опціонально)
- **Analytics**: Google Tag Manager (GTM-W3R2BGTT)
- **AI features**: Lovable AI (для майбутніх features, поки не використовуємо)

### 3.4 Локалізація

- **Мови**: EN (default), UA
- **Бібліотека**: react-i18next
- **Стратегія перекладу**: JSON файли з перекладами (/locales/en.json, /locales/ua.json)
- **URL structure**:
  - EN (default): https://midos.io/
  - UA: https://midos.io/ua/
  - Приклад: midos.io/about (EN), midos.io/ua/about (UA)

---

## 4. СТРУКТУРА КОНТЕНТУ ТА СТОРІНОК

### 4.1 Головна (/)

**Секції**:

1. Hero
   - **Заголовок EN**: "One-on-one with everyone, all at the same time."
   - **Заголовок UA**: "Особисто з кожним. Одночасно з усіма."
   - **Підзаголовок EN**: "Your AI twin works in the digital world, while you live in reality."
   - **Підзаголовок UA**: "Ваш AI-близнюк працює в цифрі, а ви живете в реальності."
   - **CTA кнопки**:
     - Primary: "Book a Demo Call" (EN) / "Забронювати демопоказ" (UA) → /demo
     - Secondary: "Watch Demo" (EN) / "Подивитись демо" (UA) → відео або /demo#video

2. Features (key benefits)
   - **Feature 1**:
     - EN: "Your AI twin knows everything you know" - "Answers 100+ questions daily. In your voice. With your expertise. While you do what you love."
     - UA: "Ваш AI-близнюк, знає все, що і ви" - "Відповідає на 100+ запитів щодня. Вашим голосом. З вашою експертизою. Поки ви робите те, що любите."

   - **Feature 2**:
     - EN: "Unlimited personal conversations simultaneously" - "Every client gets personal attention and an individual approach. Whether there's 10 or 10,000 of them."
     - UA: "Безмежна кількість особистих розмов одночасно" - "Кожен клієнт отримує персональну увагу та індивідуальний підхід. Незалежно від того, їх 10 чи 10,000."

   - **Feature 3**:
     - EN: "Works 24/7 while you live your life" - "Your digital twin doesn't sleep, eat, or take days off. Always available. You get back 20+ hours every week. For creativity. For family. For yourself."
     - UA: "Працює 24/7, поки ви живете своїм життям" - "Ваш цифровий близнюк не спить, не їсть, не бере вихідні. Він завжди на зв'язку. Ви повертаєте собі 20+ годин щотижня. Для творчості. Для сім'ї. Для себе."

3. How it works
   - **Step 1 EN**: "Share your knowledge" - "Upload documents, recordings, or connect your content sources"
   - **Step 1 UA**: "Поділіться знаннями" - "Завантажте документи, записи або підключіть джерела контенту"

   - **Step 2 EN**: "We build your digital twin" - "AI learns your voice, style, and expertise"
   - **Step 2 UA**: "Ми створюємо вашого цифрового близнюка" - "AI вивчає ваш голос, стиль та експертизу"

   - **Step 3 EN**: "Scale your impact" - "Your twin handles conversations while you focus on what matters"
   - **Step 3 UA**: "Масштабуйте вплив" - "Ваш близнюк веде розмови, поки ви зосереджені на важливому"

4. Social proof (testimonials/metrics)
   - <!-- MVP STAGE: Testimonials не показуємо, поки немає клієнтів -->
   - Показуємо: "Trusted by experts in" + список індустрій (Coaching, Consulting, Technology, Business)
   - Показуємо: Інтеграції (CRM, Calendars, Messengers logos)

5. Pricing
   - НЕ показуємо pricing tiers
   - Секція: "Get Custom Pricing" з CTA "Book a Demo Call"

6. Final CTA
   - **EN**: "Ready to get your life back? Book a demo call and see how MIDOS works for you."
   - **UA**: "Готові повернути собі життя? Забронюйте демопоказ та подивіться, як MIDOS працює для вас."

### 4.2 Бронювання (/demo)

**Функціонал**:

- [X] Заповнення форми
- [ ] Вибір експерта - НІ (немає на MVP)
- [ ] Вибір дати/часу - НІ (форма відправляється в Zoho CRM, потім менеджер зв'язується)
- [ ] Оплата - НІ
- [X] Email підтвердження - ТАК (автоматичний email після submit)

**Поля форми**:
1. Full Name (обов'язково)
2. Email (обов'язково)
3. Phone (опціонально)
4. Company (опціонально)
5. Message / How can we help? (textarea, опціонально)
6. Hidden fields: UTM params (source, medium, campaign), page referrer

**Інтеграція**: Zoho CRM API - відправка даних після submit

### 4.3 Експерти/Industries (/industries/*)

**Шаблони**:

- Список індустрій: coaches, experts, executives, podcasts, authors, consultants
- Структура сторінки індустрії:
  - Hero (заголовок специфічний для індустрії, наприклад "MIDOS for Coaches")
  - Pain points для цієї категорії (3-4 основні проблеми)
  - Solutions (як MIDOS вирішує ці проблеми)
  - Use cases (2-3 приклади використання)
  - Features relevant для цієї індустрії
  - CTA для бронювання demo

**Контент для кожної індустрії**: <!-- CONTENT_PLACEHOLDER: Буде надано окремими файлами -->

### 4.4 Blog (/blog)

**Функціонал**:

- [X] Список статей з пагінацією (12 статей на сторінку)
- [ ] Фільтри по категоріях - поки НІ (додати пізніше)
- [ ] Пошук - поки НІ (додати Phase 2)
- [X] Сторінка окремої статті
- [X] Зберігати в: Supabase database (таблиця blog_posts)

**Категорії blog**: AI Insights, Product Updates, Industry Trends, Customer Success (коли з'являться клієнти)

**Готові статті**:
1. "The Clone Economy" - адаптувати з https://www.delphi.ai/blog/the-clone-economy

### 4.5 About (/about)

**Секції**:

- **Наша історія**:
  - EN: "It started at 2:47 AM on June 1st, 2025, at a kitchen table. Founder Yuriy Boh was answering repetitive client emails about marketing positioning instead of sleeping. He compiled decades of professional knowledge into one document and uploaded it to AI. When he asked: 'How to build a marketing strategy for a psychologist?' - AI responded with striking clarity: his words, his thinking structure, his examples. That revelation sparked a key question: What if every expert could transfer their knowledge into a digital version capable of serving thousands simultaneously while they live their real lives?"
  - UA: "Все почалося 1 червня 2025 року о 2:47 ранку, за кухонним столом. Засновник Юрій Бог відповідав на повторювані клієнтські email'и про маркетингове позиціонування замість сну. Він зібрав десятиліття професійних знань в один документ і завантажив в AI. Коли він запитав: 'Як побудувати маркетингову стратегію для психолога?' — AI відповів з вражаючою ясністю: його слова, його структура мислення, його приклади. Це одкровення викликало ключове питання: Що якщо кожен експерт може перенести свої знання в цифрову версію, здатну обслуговувати тисячі одночасно, поки вони живуть своїм реальним життям?"

- **Наша місія**:
  - EN: "Free from repetition. Scale impact. Return life."
  - UA: "Звільнити від повторень. Масштабувати вплив. Жити життя."

- **Команда (якщо показувати)**: НІ - окрема сторінка /team

- **Values**:
  1. "We don't sell technology. We return experts their right to own life."
  2. "Liquid Mercury concept - flexible inside, clear solution outside"
  3. "Your gold is not metal. Your gold is time, creativity, freedom."

### 4.6 Документація (/docs/*)

**Структура** (як docs.delphi.ai):

- **Getting Started**
  - Quickstart (/docs/getting-started/quickstart)
  - Studio Navigation (/docs/getting-started/studio-navigation)
- **Build Your Digital Twin** (майбутній контент)
- **Integrations** (майбутній контент)
- **FAQs** (/docs/faq)

**Технологія**: Markdown файли + sidebar navigation компонент

### 4.7 Team (/team)

**Члени команди**:

- **Yuriy Boh**:
  - Роль: CEO & Co-Founder
  - Bio EN: "Chief Marketing Officer. Visionary behind MIDOS concept."
  - Bio UA: "Старший по маркетингу. Візіонер концепції MIDOS."
  - Фото: [TEAM_PHOTO_YURIY_BOH] <!-- IMAGE_REQUIRED: 3:4 aspect ratio -->

- **Yana Barko**:
  - Роль: COO & Co-Founder
  - Bio EN: "Chief Operating Officer. Ensures everything runs smoothly."
  - Bio UA: "Старша по порядку. Забезпечує безперебійну роботу."
  - Фото: [TEAM_PHOTO_YANA_BARKO] <!-- IMAGE_REQUIRED: 3:4 aspect ratio -->

- **Dmytro Zahorulko**:
  - Роль: CTO & Co-Founder
  - Bio EN: "Chief Technology Officer. Builds the technology behind MIDOS."
  - Bio UA: "Старший по технічній частині. Будує технологію MIDOS."
  - Фото: [TEAM_PHOTO_DMYTRO_ZAHORULKO] <!-- IMAGE_REQUIRED: 3:4 aspect ratio -->

### 4.8 Careers (/careers)

**Контент**:

- **Чому ми**:
  - EN: "Join us in building the future where experts can scale their impact without sacrificing their lives. We're a small, ambitious team working on transformative AI technology."
  - UA: "Приєднуйтесь до нас у створенні майбутнього, де експерти можуть масштабувати свій вплив, не жертвуючи життям. Ми невелика амбітна команда, що працює над трансформаційними AI технологіями."

- **Відкриті позиції**: "Coming soon" або "No open positions at the moment. Send your CV to careers@midos.io"

- **Культура компанії**:
  - Remote-first
  - Focus on impact over hours
  - Work-life balance (we practice what we preach)

### 4.9 Legal Pages

- **/terms-of-use**: <!-- LEGAL_CONTENT: Використати шаблон або адаптувати з Delphi -->
- **/privacy-policy**: <!-- LEGAL_CONTENT: GDPR compliance, cookies, data usage. Адаптувати з Delphi -->
- **/cookies**: Cookie policy - які cookies використовуємо (GTM, analytics, authentication)

### 4.10 Authentication

- **/signin**: Email/Password форма + "Sign in with Google" button
- **/signup**: Реєстраційна форма (Full Name, Email, Password, Confirm Password) + "Sign up with Google"
- **Redirect after login**: /thank-you (для MVP), пізніше /dashboard

### 4.11 Marketing Pages

- **/quiz**: 7-питальний квіз для лідогенерації → після проходження redirect на /thank-you
- **/mob-lp**: Мобільна лендінг-форма з динамічним заголовком (залежить від UTM міток) → після submit redirect на /thank-you
- **/thank-you**: Сторінка подяки після submit будь-якої форми (demo, quiz, mob-lp, signup)
- **/roi**: ROI калькулятор - інтерактивний (вхідні дані: # клієнтів, погодинна ставка, години на повторюваній роботі → вихід: "MIDOS saves you $X/month")

### 4.12 Error Pages

- **/404**:
  - Messaging EN: "Page not found. Looks like this page took a vacation."
  - Messaging UA: "Сторінку не знайдено. Схоже, ця сторінка пішла у відпустку."
  - Helpful Links: Homepage, Demo, About, Contact
  - CTA: "Go to Homepage" з автоматичним redirect через 5 секунд

- **/500**:
  - Messaging EN: "Something went wrong on our end. We're fixing it."
  - Messaging UA: "Щось пішло не так з нашого боку. Ми вже виправляємо."
  - Support Contact: support@midos.io

### 4.13 Technical Pages

- **/status**: Статус роботи системи (uptime, incidents) - можна використати https://www.statuspage.io/ або простий статичний індикатор
- **/faq**: Часті питання - список з accordion

---

## 5. 21ST.DEV КОМПОНЕНТИ ДЛЯ ІНТЕГРАЦІЇ

### 5.1 Обрані компоненти

**Список компонентів з 21st.dev для використання**:

1. **Hero Section with Video Background** - https://21st.dev/components/hero - для головної сторінки
2. **Feature Cards Grid** - https://21st.dev/components/features - для секції features на homepage
3. **Testimonials Carousel** - https://21st.dev/components/testimonials - для майбутнього (коли будуть відгуки)
4. **CTA Section** - https://21st.dev/components/cta - для final CTA на всіх сторінках
5. **Contact Form** - https://21st.dev/components/forms - для /demo та /contact
6. **FAQ Accordion** - https://21st.dev/components/accordion - для /faq сторінки
7. **Team Grid** - https://21st.dev/components/team - для /team сторінки

### 5.2 Адаптація під бренд

**Що змінити в компонентах 21st.dev**:

- Кольори → змінити на MIDOS палітру (#0066FF, #7928CA, #3D25D3)
- Шрифти → Alegreya Sans для заголовків, Inter для тексту
- Анімації → зберегти, але зменшити інтенсивність (subtle animations)
- Spacing → відповідно mobile-first (більше padding на mobile)

---

## 6. ФУНКЦІОНАЛЬНІ ВИМОГИ

### 6.1 Аутентифікація та ролі

**Ролі користувачів**:

- [X] Guest (не залогінені) - доступ до всіх публічних сторінок
- [X] Client (залогінені клієнти) - доступ до dashboard (майбутнє), профіль
- [ ] Expert - НІ для MVP
- [ ] Admin - НІ для MVP (адмінка буде окремо)

**Що доступно кожній ролі**:
- Guest: всі сторінки крім /dashboard
- Client: все + /dashboard (майбутнє)

### 6.2 Система бронювання

**Core flow**:

1. Користувач заходить на /demo
2. Заповнює форму (Name, Email, Phone, Company, Message)
3. Натискає "Book Demo Call"
4. Дані відправляються в Zoho CRM через API
5. Користувач бачить /thank-you сторінку
6. Автоматичний email підтвердження (опціонально)
7. Менеджер з Zoho CRM зв'язується з лідом для призначення дати/часу demo

**Notifications**: Email підтвердження (через Supabase або Resend)

**Cancellation policy**: Немає (бо немає fixed appointments на цьому етапі)

**Rescheduling**: НІ (менеджер домовляється напряму з лідом)

### 6.3 AI Features

- [ ] AI scheduling assistant - НІ для MVP
- [ ] Chatbot - НІ для MVP (можливо Phase 2)
- [ ] Content generation - НІ для MVP
- [ ] Digital Twin demo - можливо Phase 2 (показати демо на сайті)

**Використати**: Lovable AI models (якщо потрібно в майбутньому)

### 6.4 SEO та Performance

**Meta titles/descriptions для кожної сторінки**:

- **Homepage**:
  - Title EN: "MIDOS - Scale Your Expertise with AI Digital Twin | 24/7 Personal Clone"
  - Title UA: "MIDOS - Масштабуйте експертизу з AI близнюком | Цифровий клон 24/7"
  - Description EN: "Your AI twin answers 100+ questions daily. In your voice. With your expertise. Get back 20+ hours every week. Book a demo call."
  - Description UA: "Ваш AI-близнюк відповідає на 100+ запитів щодня. Вашим голосом. З вашою експертизою. Поверніть собі 20+ годин щотижня. Забронюйте демопоказ."

- **About**:
  - Title: "About MIDOS - Our Mission to Return Life to Experts"
  - Description: "Born at 2:47 AM from a simple question: What if every expert could scale their impact without sacrificing their life?"

- **Demo**:
  - Title: "Book a Demo Call - See MIDOS in Action"
  - Description: "Get a personalized demo and see how MIDOS can save you 20+ hours every week. No commitment required."

- **Open Graph images**: ТАК - створити OG image 1200x630px для кожної основної сторінки

- **Structured data (JSON-LD)**: ТАК
  - Organization schema для homepage
  - Article schema для blog posts
  - FAQPage schema для /faq

- **Sitemap**: AUTO-GENERATED через sitemap.xml

- **robots.txt**:
```
User-agent: *
Allow: /
Disallow: /admin/
Disallow: /api/
Sitemap: https://midos.io/sitemap.xml
```

---

## 7. TIMELINE ТА ПРІОРИТЕТИ

### 7.1 MVP (Minimum Viable Product)

**Must-have для launch**:

- [X] Головна сторінка (/)
- [X] Demo booking flow (/demo → /thank-you)
- [X] About page (/about)
- [X] Team page (/team)
- [X] Contact page (/contact)
- [X] Authentication (Sign in/Sign up)
- [X] Industries pages (6 сторінок) - базові версії
- [X] Legal pages (Privacy, Terms)
- [X] GTM integration для analytics
- [X] Zoho CRM integration для demo форми
- [X] Mobile-first responsive design
- [X] UA/EN localization

**Deadline MVP**: <!-- DEADLINE: To be defined by client -->

### 7.2 Phase 2

**Nice-to-have**:

- [ ] Blog з 2-3 статтями
- [ ] Документація (базові розділи Getting Started)
- [ ] Quiz для лідогенерації
- [ ] Mobile LP з UTM tracking
- [ ] ROI калькулятор
- [ ] FAQ сторінка
- [ ] Search functionality для blog/docs

### 7.3 Phase 3

**Future enhancements**:

- [ ] Partner portal (partner.midos.io)
- [ ] Client dashboard
- [ ] Digital Twin demo widget на сайті
- [ ] Chatbot
- [ ] Mobile app
- [ ] Додаткові інтеграції (Calendly, Stripe)
- [ ] Advanced analytics dashboard

---

## 8. КОНТЕНТ-ДЖЕРЕЛА

### 8.1 З delphi.ai

**Що копіювати та адаптувати**:

- [X] Features descriptions → Адаптувати: замінити "Digital Mind" на "Digital Twin", змінити приклади під MIDOS use cases
- [X] Industry pages structure → Адаптувати: використати структуру, але написати новий контент для MIDOS
- [X] Legal templates → Адаптувати: Privacy Policy та Terms of Use змінити назву компанії, контакти
- [X] Blog article "The Clone Economy" → Адаптувати: переписати під MIDOS, змінити приклади

### 8.2 Власний контент

**Що писати з нуля**:

- Brand story (історія про 2:47 AM)
- Team bios (короткі біо засновників)
- Mission statement та philosophy
- Use cases специфічні для MIDOS
- Industries контент для 6 сторінок

### 8.3 Медіа-ресурси

- **Зображення**: Unsplash (технологічні, люди з пристроями) + власні фото команди (коли будуть)
- **Ілюстрації**: Створити custom (концепція Liquid Mercury) або використати з 21st.dev
- **Відео**: НІ для MVP (можливо Phase 2 - demo відео)
- **Іконки**: Lucide React ✓

---

## 9. DESIGN SYSTEM SPECIFICS

### 9.1 Mobile-First Breakpoints

```css
/* Tailwind CSS breakpoints */
- mobile: default (до 640px)
- sm: 640px (tablet portrait)
- md: 768px (tablet landscape)
- lg: 1024px (desktop)
- xl: 1280px (large desktop)
- 2xl: 1536px (extra large desktop)
```

### 9.2 Component Patterns

**Повторювані UI patterns**:

- **Card style**: З тінню (shadow-card), border-radius 12px, білий фон
- **Button hierarchy**:
  - Primary: #7eeb26 (bright green), білий текст, bold
  - Secondary: білий фон, #0066FF border, #0066FF текст
  - Ghost: прозорий, #0066FF текст, без border
- **Form inputs**: border 1px solid #6c757d, border-radius 4px, focus: border #0066FF + shadow
- **Navigation**: Sticky header, horizontal menu desktop, hamburger mobile

### 9.3 Spacing System

- **Base unit**: 4px (Tailwind default)
- **Section padding mobile**: py-12 px-4 (48px vertical, 16px horizontal)
- **Section padding desktop**: py-20 px-8 (80px vertical, 32px horizontal)
- **Container max-width**: 1280px (max-w-7xl)

---

## 10. NOTES ТА CONSTRAINTS

### 10.1 Technical Constraints

- **Maximum file size uploads**: 10MB (для demo форми attachments, якщо додамо)
- **Browser support**: Останні 2 версії Chrome, Firefox, Safari, Edge
- **Mobile support**: iOS 14+, Android 10+

### 10.2 Content Guidelines

- **Max heading length**: 60 characters (для SEO titles)
- **Max paragraph length**: 150-200 слів (для читабельності)
- **Image aspect ratios**:
  - Hero: 16:9
  - Cards: 4:3
  - Team photos: 3:4
  - OG images: 1.91:1 (1200x630px)

### 10.3 Navigation Structure

#### Header Navigation (Global)
- **Logo** → Homepage (/)
- **Industries** → Dropdown menu
  - Coaches → /industries/coaches
  - Experts → /industries/experts
  - Executives → /industries/executives
  - Podcasts → /industries/podcasts
  - Authors → /industries/authors
  - Consultants → /industries/consultants
- **About** → /about
- **Blog** → /blog
- **Docs** → https://docs.midos.io
- **CTA Button** → "Book Demo" → /demo

#### Footer Navigation

**[Column 1: Product]**
- Features → /#features
- Industries → /industries/coaches
- ROI Calculator → /roi
- Book Demo → /demo

**[Column 2: Company]**
- About → /about
- Team → /team
- Careers → /careers
- Blog → /blog

**[Column 3: Resources]**
- Documentation → https://docs.midos.io
- Help Center → https://docs.midos.io
- FAQ → /faq
- Status → /status

**[Column 4: Legal]**
- Privacy Policy → /privacy-policy
- Terms of Use → /terms-of-use
- Cookies → /cookies

**[Footer Bottom]**
- © 2025 MIDOS.IO. All rights reserved.
- Social media icons: LinkedIn, Instagram, Twitter, Facebook, YouTube, TikTok, Telegram

#### Mobile Navigation
- Hamburger menu (з усіма пунктами з desktop)
- Language switcher (EN/UA)
- Sticky "Book Demo" button внизу екрану

---

## 11. DODATKOVI TEHNICHNI VYMOGY

### 11.1 Google Tag Manager Setup

**GTM Container ID**: GTM-W3R2BGTT

**Events to track**:
- page_view (всі сторінки)
- demo_form_submit (форма /demo)
- quiz_start (початок квізу)
- quiz_complete (завершення квізу)
- signup_complete (реєстрація)
- signin_complete (вхід)
- cta_click (клік на будь-яку CTA кнопку)
- outbound_link_click (клік на зовнішні посилання)

### 11.2 Zoho CRM Integration

**API Endpoint**: Zoho CRM API для створення Leads

**Fields mapping**:
- Full Name → First Name + Last Name (split)
- Email → Email
- Phone → Phone
- Company → Company
- Message → Description
- Source → Lead Source (наприклад: "Website Demo Form")
- UTM params → Custom fields

### 11.3 User Flow

**Flow 1: UA/EN Language Detection**
- Лід потрапляє на midos.io (EN default) або midos.io/ua
- Language switcher в header для зміни мови
- Localization зберігається в localStorage

**Flow 2: Demo Booking**
1. Лід клікає "Book Demo" на будь-якій сторінці
2. Перенаправлення на /demo (або /ua/demo)
3. Заповнює форму
4. Submit → дані в Zoho CRM
5. Redirect на /thank-you (або /ua/thank-you)

**Flow 3: Mobile LP**
1. Лід з реклами потрапляє на /mob-lp?utm_source=...
2. Динамічний заголовок залежно від UTM
3. Заповнює mini форму
4. Redirect на /thank-you

**Flow 4: Quiz**
1. Лід потрапляє на /quiz
2. Проходить 7 питань
3. Submit на останньому кроці
4. Redirect на /thank-you

**Flow 5: Sign In/Sign Up**
1. Лід клікає "Sign In" або "Sign Up"
2. Заповнює форму
3. Після успішної автентифікації → redirect на /thank-you (для MVP)
4. В майбутньому → redirect на /dashboard

---

## 12. ACCESSIBILITY & PERFORMANCE

### 12.1 Accessibility (WCAG 2.1 AA)

- Color contrast: мінімум 4.5:1 для тексту
- Keyboard navigation: всі інтерактивні елементи доступні через Tab
- ARIA labels: для всіх form inputs, buttons, navigation
- Alt text: для всіх зображень
- Focus indicators: видимі для всіх інтерактивних елементів

### 12.2 Performance Targets

- **Lighthouse Score**: 90+ (Performance, Accessibility, Best Practices, SEO)
- **Core Web Vitals**:
  - LCP (Largest Contentful Paint): < 2.5s
  - FID (First Input Delay): < 100ms
  - CLS (Cumulative Layout Shift): < 0.1
- **Page load time**: < 3s на 3G
- **Image optimization**: WebP format, lazy loading

---

**End of MIDOS Knowledge Base**

<!-- LAST UPDATED: November 13, 2025 -->
<!-- VERSION: 1.0 MVP -->
<!-- STATUS: READY FOR DEVELOPMENT -->
