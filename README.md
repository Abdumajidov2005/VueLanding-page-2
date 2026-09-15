# Portfolio — Vue 3 + Tailwind

Figma dizayndan (portfolio sahifasi) qurilgan komponentlar. `vue-lessons` loyihangizga shu tarzda joylashtiring:

1. `src/App.vue` faylini mavjud `App.vue`'ga almashtiring.
2. `src/components/` papkasini o'zingizdagi `src/components/` ichiga ko'chiring:
   - `TheHeader.vue` — yuqori navigatsiya
   - `HeroSection.vue` — "Hello, I'm Gleb Kostrubov" bo'limi (aylana surat + belgi ikonalari)
   - `ServicesSection.vue` — xizmatlar kartochkalari (7 ta)
   - `AboutSection.vue` — "About me" bo'limi (rasm kolajlari + yoy dekoratsiyalari)
   - `PortfolioSection.vue` — loyihalar karuseli (oldinga/orqaga tugmalari bilan, `ref()` orqali reaktiv)
   - `TheFooter.vue` — pastki qism

## Rasm/foto joylari

Original dizaynda haqiqiy fotosuratlar bor edi, men esa ularni placeholder qildim:

- `HeroSection.vue` ichida `/images/hero-photo.png` — asosiy portret
- `AboutSection.vue` ichida `/images/about-1.jpg`, `about-2.jpg`, `about-3.jpg` — kolaj rasmlari

`public/images/` papkasiga o'z rasmlaringizni qo'yib, shu yo'llarni moslang.

## Tailwind

Loyihangizda Tailwind allaqachon o'rnatilgan bo'lsa, qo'shimcha konfiguratsiya kerak emas — barcha ranglar `bg-[#hex]` tarzida arbitrary value sifatida yozilgan, `tailwind.config.js`ga custom rang qo'shish shart emas.

Agar shrift sifatida "Manrope" ishlatmoqchi bo'lsangiz, `index.html`ga qo'shing:

```html
<link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

va `tailwind.config.js`da `fontFamily.sans`ni shunga o'rnating.

## Interaktivlik

`PortfolioSection.vue` ichida `ref()` bilan `current` state va `next()`/`prev()` funksiyalari bor — bu Vue'da o'rgangan `v-for`, `v-bind`, `@click` mavzularingizga mos amaliy misol.
