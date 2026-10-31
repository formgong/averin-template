# Averin: a private multi-specialty clinic site with a Formgong form

**Live demo:** https://averin.formgong.com · Download: the [latest release](https://github.com/formgong/averin-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/averin-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Faverin-template&project-name=averin&repository-name=averin)

Each button copies the site to your GitHub and publishes it. Then replace `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Сайт приватної багатопрофільної клініки з формою запису Формгонг

A bright one-page site for a private clinic with family doctors, check-ups, a lab and specialists, in a single `index.html` plus an `img/` folder. The demo clinic, Averin, its doctors, address, prices, numbers and reviews are fictional sample content.

- **Header.** Logo, menu and a lime "Book a visit" button. "Services" opens a wide menu with all six services and a featured check-up card. The header hides when you scroll down and comes back when you scroll up. On phones and tablets a "Menu" button opens a full-screen green menu.
- **Hero.** A large botanical photo in a rounded frame beside a serif headline that fades in word by word, two buttons and three short facts.
- **Why Averin.** A dark green panel with two lines of huge type that drift sideways as you scroll, a statement whose words light up one by one, and three numbers that count up.
- **Services.** Six cards (family doctor, check-ups, diagnostics and lab, specialists, IV and vitamin therapy, video visits) with a photo, tags and a starting price. A click on a card picks that service in the form.
- **How a visit works.** Four steps. On wide screens the photo on the left stays in place and changes with the step you are reading, with a large step counter.
- **Specialties.** A lime band with the specialties running across.
- **Doctors.** Four portraits that open from the bottom, with working days, role and languages, then a panel about the building.
- **Prices.** A green membership card and a price list in three groups.
- **Reviews.** Six patient quotes in a masonry grid.
- **FAQ.** Seven questions that open and close.
- **Booking.** Address, phone, email, hours, an emergency note, and the appointment request form.
- **Footer.** Links, address, contact, and a giant wordmark.

Blocks rise into view as you scroll and headings come up word by word. With `prefers-reduced-motion: reduce` nothing moves and everything is visible at once. Without JavaScript all content is visible too.

## English

**Set up the form**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace `fk_your_access_key` with that key.
3. The form sends `name`, `email`, `phone`, `service`, `day`, `time`, `message`, a hidden `subject` and the hidden spam trap `botcheck`. Name and email are required; the rest is optional. `service` is one of Family doctor, Check-up, Lab tests, Specialist, IV therapy, Video visit, Membership. It shows thanks only when Formgong answers `success: true`. If the answer is anything else, it shows the error and keeps what was typed.

**Health data.** This form is for appointment requests. Don't use it to collect diagnoses, medical history, prescriptions or insurance numbers; keep those in your clinic's own patient system. The note field already asks people not to include medical details.

**Edit**

- Colours are at the top of the styles: `--forest` for the dark panels, `--lime` for buttons and highlights, `--bg`, `--mint` and `--tint` for the light backgrounds, `--ink` for text. Fonts are Instrument Serif (headings) and Bricolage Grotesque (everything else), both from Google Fonts.
- Services are `<article class="svc">` cards. The `data-service` value on a card's button must match one of the `service` options in the form.
- Steps are `<li class="step" data-step="…">`, and the photos that change with them are `<div class="ph" data-shot="…">` with the same numbers.
- Numbers that count up use `data-count`.
- Doctors, prices, reviews and the address are sample content. Replace them with your own before launch.

**Images.** The twelve photos were generated for this template with ChatGPT image generation (OpenAI) and saved as WebP, about 880 KB in all. The people and places are fictional. The prompts are in `img-prompts.json`. You may use the photos in your own site, but replace them with photos of your own clinic and team before launch. Until a photo is there, its frame shows a soft green placeholder.

The "Powered by Formgong" links point to `https://formgong.com/review-page/fk_your_access_key`, so the same find and replace covers them. Once your key is in, the first click from your published site makes your own public review page on Formgong, where clients read and leave reviews, and every later click opens it. Switch the page off in Formgong (Reviews → your site → Settings) or change those links.

## Українська

Світлий односторінковий сайт для приватної клініки: сімейні лікарі, чекапи, лабораторія і вузькі спеціалісти. Клініка Averin, лікарі, адреса, ціни, цифри та відгуки вигадані, це зразок вмісту.

На сторінці:

- шапка з меню «Послуги» на всю ширину; під час прокрутки вниз вона ховається, а вгору повертається; на телефоні кнопка «Menu» відкриває зелене меню на весь екран;
- перший екран з великим фото рослини та заголовком, що проявляється слово за словом;
- темно-зелений блок «Why Averin»: великі рядки зсуваються вбік під час прокрутки, слова тексту засвічуються одне за одним, цифри рахуються;
- шість карток послуг: клік по картці вибирає цю послугу у формі;
- чотири кроки візиту, фото ліворуч стоїть на місці й змінюється разом із кроком;
- лаймова стрічка зі спеціалізаціями;
- четверо лікарів і блок про будівлю клініки;
- членство та прайс у трьох групах;
- шість відгуків пацієнтів;
- сім запитань, що розгортаються;
- запис: адреса, телефон, години роботи, примітка про невідкладні випадки та форма;
- футер з великим логотипом.

**Налаштування форми.** Створіть форму в кабінеті Formgong і замініть `fk_your_access_key` у `index.html` на свій ключ. Форма надсилає `name`, `email`, `phone`, `service`, `day`, `time`, `message`, прихований `subject` і пастку для спаму `botcheck`. Обов'язкові лише ім'я та email. Подяка з'являється лише тоді, коли Formgong відповідає `success: true`; інакше форма показує помилку й не стирає введене.

**Медичні дані.** Ця форма лише для запису на прийом. Не збирайте через неї діагнози, історію хвороби, рецепти чи номери страховок; зберігайте їх у власній системі клініки для пацієнтів. Поле для коментаря вже просить не писати медичних подробиць.

**Редагування.** Кольори на початку стилів: `--forest` для темних блоків, `--lime` для кнопок і акцентів, `--bg`, `--mint` і `--tint` для світлих фонів. Шрифти: Instrument Serif і Bricolage Grotesque з Google Fonts. Значення `data-service` на кнопці картки має збігатися з одним із варіантів `service` у формі. Лікарі, ціни, відгуки й адреса є зразком, замініть їх своїми перед запуском.

**Зображення:** дванадцять фото згенеровано для цього шаблону в ChatGPT (OpenAI) і збережено у WebP, разом близько 880 КБ. Люди й місця вигадані, промпти лежать у `img-prompts.json`. Фото можна використовувати, але перед запуском замініть їх знімками своєї клініки та команди. Поки фото немає, у рамці видно м'яку зелену заглушку.

MIT license.

Посилання «Powered by Formgong» ведуть на `https://formgong.com/review-page/fk_your_access_key`, тож та сама заміна ключа оновить і їх. Коли ключ стоїть, перший перехід з вашого опублікованого сайту створює вашу публічну сторінку відгуків на Formgong, де клієнти читають і залишають відгуки; далі посилання відкриває її. Вимкнути сторінку можна у Formgong (Відгуки → ваш сайт → Налаштування) або змінити ці посилання.
