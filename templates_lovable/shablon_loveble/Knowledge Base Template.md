# SmartBook Platform - Knowledge Base Template (MECE)

## 1. БІЗНЕС-КОНТЕКСТ

### 1.1 Проект

- **Назва проекту**: [ЗАПОВНИТИ]
- **Слоган/Tagline**: [ЗАПОВНИТИ]
- **Місія**: [ЗАПОВНИТИ]
- **Конкурент для аналізу**: delphi.ai
- **Унікальна пропозиція (USP)**: [ЗАПОВНИТИ]

### 1.2 Цільова аудиторія

- **Основна ЦА**: [ЗАПОВНИТИ - приклад: професійні коучі, консультанти, експерти]
- **Вторинна ЦА**: [ЗАПОВНИТИ]
- **Pain points**: [ЗАПОВНИТИ]
- **Jobs to be done**: [ЗАПОВНИТИ]

### 1.3 Бізнес-модель

- **Тип**: [ЗАПОВНИТИ - SaaS / Marketplace / Platform]
- **Монетизація**: [ЗАПОВНИТИ - підписка / комісія / freemium]
- **Pricing tiers**: [ЗАПОВНИТИ]

---

## 2. БРЕНД ТА ВІЗУАЛЬНА ІДЕНТИЧНІСТЬ

### 2.1 Brand Voice & Tone

- **Характер бренду**: [ЗАПОВНИТИ - приклад: професійний, дружній, інноваційний]
- **Tone of voice UA**: [ЗАПОВНИТИ]
- **Tone of voice EN**: [ЗАПОВНИТИ]
- **Заборонені слова/фрази**: [ЗАПОВНИТИ]

### 2.2 Дизайн-система (Базові значення)

```css
/* КОЛЬОРИ - заповніть HSL значення */
--primary: [ЗАПОВНИТИ - приклад: 220 90% 56%];
--primary-foreground: [ЗАПОВНИТИ];
--secondary: [ЗАПОВНИТИ];
--accent: [ЗАПОВНИТИ];
--background: [ЗАПОВНИТИ];
--foreground: [ЗАПОВНИТИ];
--muted: [ЗАПОВНИТИ];
--border: [ЗАПОВНИТИ];

/* ГРАДІЄНТИ */
--gradient-primary: [ЗАПОВНИТИ - приклад: linear-gradient(135deg, hsl(220 90% 56%), hsl(280 90% 56%))];
--gradient-hero: [ЗАПОВНИТИ];

/* ТІНІ */
--shadow-elegant: [ЗАПОВНИТИ];
--shadow-card: [ЗАПОВНИТИ];
```

### 2.3 Типографіка

- **Primary font**: [ЗАПОВНИТИ - приклад: Inter]
- **Weights used**: [ЗАПОВНИТИ - приклад: 200, 300, 400, 600]
- **Heading style**: [ЗАПОВНИТИ - tight/normal/loose tracking]
- **Body style**: [ЗАПОВНИТИ]

### 2.4 Анімації та Interaction

- **Animation style**: [ЗАПОВНИТИ - subtle / energetic / minimal]
- **Transition timing**: [ЗАПОВНИТИ - приклад: 0.3s ease-out]
- **Hover effects**: [ЗАПОВНИТИ]
- **Scroll animations**: [TAK/NI]

---

## 3. ТЕХНІЧНИЙ СТЕК ТА АРХІТЕКТУРА

### 3.1 Frontend

- **Framework**: React + Vite + TypeScript ✓
- **Styling**: Tailwind CSS ✓
- **Animations**: GSAP + Three.js ✓
- **Component library**: shadcn/ui + 21st.dev components ✓
- **State management**: [ЗАПОВНИТИ - React Query / Zustand / Context]

### 3.2 Backend & Database

- **Backend**: Lovable Cloud (Supabase) ✓
- **Authentication**: [ЗАПОВНИТИ - email/password / OAuth / magic link]
- **Database structure**: [ЗАПОВНИТИ - список основних таблиць]
  - users/profiles
  - experts
  - bookings
  - [ДОДАТИ ІНШІ]

### 3.3 Інтеграції

- **Calendar**: [ЗАПОВНИТИ - Google Calendar / Calendly API / власна]
- **Payments**: [ЗАПОВНИТИ - Stripe / LiqPay / не потрібно]
- **Email**: [ЗАПОВНИТИ - Resend / SendGrid / Supabase Auth]
- **Analytics**: [ЗАПОВНИТИ - Google Analytics / Plausible / не потрібно]
- **AI features**: [ЗАПОВНИТИ - Lovable AI / OpenAI / не потрібно]

### 3.4 Локалізація

- **Мови**: EN (default), UA
- **Бібліотека**: [ЗАПОВНИТИ - react-i18next / next-intl / власне рішення]
- **Стратегія перекладу**: [ЗАПОВНИТИ - файли JSON / database / CMS]
- **URL structure**: [ЗАПОВНИТИ - /en/page, /ua/page або /?lang=ua]

---

## 4. СТРУКТУРА КОНТЕНТУ ТА СТОРІНОК

### 4.1 Головна (/)

**Секції**:

1. Hero
   - **Заголовок EN**: [ЗАПОВНИТИ]
   - **Заголовок UA**: [ЗАПОВНИТИ]
   - **Підзаголовок EN**: [ЗАПОВНИТИ]
   - **Підзаголовок UA**: [ЗАПОВНИТИ]
   - **CTA кнопки**: [ЗАПОВНИТИ]

2. Features (key benefits)
   - **Feature 1**: [НАЗВА + ОПИС EN/UA]
   - **Feature 2**: [НАЗВА + ОПИС EN/UA]
   - **Feature 3**: [НАЗВА + ОПИС EN/UA]
   - **Feature 4**: [НАЗВА + ОПИС EN/UA]

3. How it works
   - **Step 1**: [ЗАПОВНИТИ EN/UA]
   - **Step 2**: [ЗАПОВНИТИ EN/UA]
   - **Step 3**: [ЗАПОВНИТИ EN/UA]

4. Social proof (testimonials/metrics)
   - [ЗАПОВНИТИ - які метрики показувати]

5. Pricing (якщо потрібно)
   - [ЗАПОВНИТИ - плани та ціни]

6. Final CTA
   - [ЗАПОВНИТИ EN/UA]

### 4.2 Бронювання (/booking або /call)

**Функціонал**:

- [ ] Вибір експерта
- [ ] Вибір дати/часу
- [ ] Заповнення форми
- [ ] Оплата (ТАК/НІ)
- [ ] Email підтвердження

**Поля форми**: [ЗАПОВНИТИ - ім'я, email, тема, тощо]

### 4.3 Експерти/Industries (/experts/_ або /industries/_)

**Шаблони**:

- Список індустрій: [ЗАПОВНИТИ - coaches, consultants, therapists, тощо]
- Структура сторінки експерта:
  - Hero (опис індустрії)
  - Benefits для цієї категорії
  - Список експертів (якщо є)
  - CTA для бронювання

**Контент для кожної індустрії**: [СТВОРИТИ ОКРЕМІ ФАЙЛИ]

### 4.4 Blog (/blog)

**Функціонал**:

- [ ] Список статей з пагінацією
- [ ] Фільтри по категоріях
- [ ] Пошук
- [ ] Сторінка окремої статті
- [ ] Зберігати в: [ЗАПОВНИТИ - database / markdown файли / CMS]

**Категорії blog**: [ЗАПОВНИТИ]

### 4.5 About (/about)

**Секції**:

- Наша історія: [ЗАПОВНИТИ EN/UA]
- Наша місія: [ЗАПОВНИТИ EN/UA]
- Команда (якщо показувати): [ТАК/НІ]
- Values: [ЗАПОВНИТИ]

### 4.6 Документація (/docs/\*)

**Структура** (як docs.delphi.ai):

- Getting Started
- [ЗАПОВНИТИ - розділи документації]
- API Reference (якщо потрібно)
- FAQs

**Технологія**: [ЗАПОВНИТИ - markdown + sidebar navigation]

### 4.7 Team (/team)

**Члени команди**:

- [ІМ'Я 1]: [РОЛЬ, BIO, ФОТО]
- [ІМ'Я 2]: [РОЛЬ, BIO, ФОТО]
- [ДОДАТИ ІНШИХ]

### 4.8 Careers (/careers)

**Контент**:

- Чому ми: [ЗАПОВНИТИ EN/UA]
- Відкриті позиції: [ЗАПОВНИТИ або "Coming soon"]
- Культура компанії: [ЗАПОВНИТИ]

### 4.9 Legal Pages

- **/terms-of-use**: [ЗАПОВНИТИ - використати шаблон або скопіювати з delphi]
- **/privacy-policy**: [ЗАПОВНИТИ - GDPR compliance, cookies, data usage]

### 4.10 Authentication

- **/login**: Email/Password форма
- **/signup**: [ТАК/НІ - чи потрібна окрема сторінка]
- **Redirect after login**: [ЗАПОВНИТИ - /dashboard або /]

---

## 5. 21ST.DEV КОМПОНЕНТИ ДЛЯ ІНТЕГРАЦІЇ

### 5.1 Обрані компоненти

**Список компонентів з 21st.dev для використання**:

1. [КОМПОНЕНТ 1 - назва, URL, для якої секції]
2. [КОМПОНЕНТ 2 - назва, URL, для якої секції]
3. [КОМПОНЕНТ 3 - назва, URL, для якої секції]
4. [ДОДАТИ ІНШІ]

### 5.2 Адаптація під бренд

**Що змінити в компонентах 21st.dev**:

- Кольори → змінити на власну палітру
- Шрифти → [ЗАПОВНИТИ]
- Анімації → [зберегти / спростити / підсилити]
- Spacing → відповідно mobile-first

---

## 6. ФУНКЦІОНАЛЬНІ ВИМОГИ

### 6.1 Аутентифікація та ролі

**Ролі користувачів**:

- [ ] Guest (не залогінені)
- [ ] Client (залогінені клієнти)
- [ ] Expert (якщо є експерти в системі)
- [ ] Admin (якщо потрібно)

**Що доступно кожній ролі**: [ЗАПОВНИТИ]

### 6.2 Система бронювання

**Core flow**:

1. [ЗАПОВНИТИ - опис процесу бронювання покроково]
2. Notifications: [email / SMS / push / все разом]
3. Cancellation policy: [ЗАПОВНИТИ]
4. Rescheduling: [ТАК/НІ]

### 6.3 AI Features (якщо потрібно)

- [ ] AI scheduling assistant
- [ ] Chatbot
- [ ] Content generation
- [ ] [ІНШІ - ЗАПОВНИТИ]

**Використати**: Lovable AI models (gemini/gpt) без API ключів

### 6.4 SEO та Performance

- **Meta titles/descriptions**: [ЗАПОВНИТИ для кожної сторінки]
- **Open Graph images**: [ТАК/НІ]
- **Structured data (JSON-LD)**: [ТАК/НІ]
- **Sitemap**: [AUTO-GENERATED]
- **robots.txt**: [ЗАПОВНИТИ rules]

---

## 7. TIMELINE ТА ПРІОРИТЕТИ

### 7.1 MVP (Minimum Viable Product)

**Must-have для launch**:

- [ ] Головна сторінка
- [ ] Booking flow
- [ ] Authentication
- [ ] [ЗАПОВНИТИ - що ще критично]

**Deadline MVP**: [ЗАПОВНИТИ - дата]

### 7.2 Phase 2

**Nice-to-have**:

- [ ] Blog
- [ ] Документація
- [ ] Додаткові індустрії
- [ ] [ЗАПОВНИТИ]

### 7.3 Phase 3

**Future enhancements**:

- [ ] Mobile app
- [ ] Додаткові інтеграції
- [ ] [ЗАПОВНИТИ]

---

## 8. КОНТЕНТ-ДЖЕРЕЛА

### 8.1 З delphi.ai

**Що копіювати та адаптувати**:

- [ ] Features descriptions → [АДАПТУВАТИ ЯК]
- [ ] Industry pages structure → [АДАПТУВАТИ ЯК]
- [ ] Legal templates → [АДАПТУВАТИ ЯК]
- [ ] [ЗАПОВНИТИ - що ще]

### 8.2 Власний контент

**Що писати з нуля**:

- Brand story
- Team bios
- [ЗАПОВНИТИ]

### 8.3 Медіа-ресурси

- **Зображення**: [ЗАПОВНИТИ - Unsplash / власні фото / AI generation]
- **Ілюстрації**: [ЗАПОВНИТИ]
- **Відео**: [ТАК/НІ]
- **Іконки**: Lucide React ✓

---

## 9. DESIGN SYSTEM SPECIFICS

### 9.1 Mobile-First Breakpoints

```
- mobile: [ЗАПОВНИТИ - default, до якого розміру]
- tablet: [ЗАПОВНИТИ - md: від якого px]
- desktop: [ЗАПОВНИТИ - lg: від якого px]
- wide: [ЗАПОВНИТИ - xl: від якого px]
```

### 9.2 Component Patterns

**Повторювані UI patterns**:

- Card style: [ЗАПОВНИТИ - з тінню / без / з border]
- Button hierarchy: [ЗАПОВНИТИ - primary/secondary/ghost styles]
- Form inputs: [ЗАПОВНИТИ - стиль]
- Navigation: [ЗАПОВНИТИ - тип меню]

### 9.3 Spacing System

- Base unit: [ЗАПОВНИТИ - 4px / 8px]
- Section padding mobile: [ЗАПОВНИТИ]
- Section padding desktop: [ЗАПОВНИТИ]

---

## 10. NOTES ТА CONSTRAINTS

### 10.1 Technical Constraints

- Maximum file size uploads: [ЗАПОВНИТИ]
- Browser support: [ЗАПОВНИТИ - останні 2 версії Chrome/Firefox/Safari]
- Mobile support: [iOS/Android версії]

### 10.2 Content Guidelines

- Max heading length: [ЗАПОВНИТИ]
- Max paragraph length: [ЗАПОВНИТИ]
- Image aspect ratios: [ЗАПОВНИТИ]

### 10.3 Navigation Structure

### Header Navigation (Global)
- Logo → Homepage (/)
- Solutions → Dropdown menu
  - Industries → /industries
  - Use Cases → /industries#use-cases
- Pricing → /pricing (або секція на homepage)
- Resources → Dropdown menu
  - Blog → /blog
  - Documentation → /docs
  - About → /about
- CTA Button → /booking

### Footer Navigation
[Column 1: Product]
- Features → /#features
- Pricing → /pricing
- Documentation → /docs

[Column 2: Company]
- About → /about
- Team → /team
- Careers → /careers

[Column 3: Legal]
- Privacy Policy → /privacy-policy
- Terms of Use → /terms-of-use

[Column 4: Resources]
- Blog → /blog
- Help Center → /docs


---


