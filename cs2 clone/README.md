# 🎮 CS2 Clone — Web Edition

> 🇬🇧 A full browser-based Counter-Strike 2 clone. One HTML file, zero dependencies, zero setup. Open and play.
>
> 🇷🇺 Полноценный клон Counter-Strike 2 прямо в браузере. Один HTML-файл, никаких зависимостей, никакой установки. Открой и играй.

![status](https://img.shields.io/badge/status-final-brightgreen)
![license](https://img.shields.io/badge/license-MIT-blue)
![three.js](https://img.shields.io/badge/three.js-r160-orange)
![adaptive](https://img.shields.io/badge/design-adaptive-success)
![i18n](https://img.shields.io/badge/docs-EN%20%2B%20RU-yellow)

---

## 📖 About / О проекте

> 🇬🇧 **CS2 Clone** is a browser-based tactical shooter that recreates the core mechanics of Counter-Strike 2 using **Three.js** and **vanilla JavaScript**. The entire engine, all logic, and all graphics live in a **single HTML file** — no installation, no build step, no internet required (after Three.js loads from CDN). This project proves complex game mechanics can exist without engines or bundlers — just a browser, WebGL, and ~3000 lines of code.
>
> 🇷🇺 **CS2 Clone** — браузерный тактический шутер, воссоздающий ключевые механики Counter-Strike 2 средствами **Three.js** и чистого **JavaScript**. Весь движок, вся логика и вся графика живут в **одном HTML-файле** — без установки, без сборки, без интернета (после загрузки Three.js из CDN). Проект показывает, что сложные игровые механики можно реализовать без движков и сборщиков — только браузер, WebGL и ~3000 строк кода.

---

## ✨ Features / Возможности

### 🎯 Gameplay / Геймплей

> 🇬🇧
> - **Two modes**: Deathmatch (13 players, 5 min) and Normal (3 vs 10 with a bomb)
> - **Three maps**: Dust, Mirage, Inferno — each with unique style, cover layout, and bomb site
> - **Tactical bots** with line-of-sight checks — no shooting through walls, they miss, flank, retreat at low HP, reposition after miss streaks
> - **Bomb** with 40 s detonation timer, 3 s plant, 5 s defuse
>
> 🇷🇺
> - **Два режима**: «Бой насмерть» (13 участников, 5 минут) и «Обычный» (3 vs 10 с бомбой)
> - **Три карты**: Пыль, Мираж, Инферно — у каждой свой стиль, расположение укрытий и точка закладки
> - **Тактические боты** с проверкой линии видимости — не стреляют сквозь стены, промахиваются, флангуют, отступают при низком HP, меняют позицию после серии промахов
> - **Бомба** с таймером 40 с, закладкой 3 с и разминированием 5 с

### 🔫 Weapons & Gear / Оружие и снаряжение

| Weapon · Оружие | Head · Голова | Body · Тело | Ammo · Боезапас |
|---|---|---|---|
| Pistol · Пистолет | 125 | 36 | ∞ (no reload · без перезарядки) |
| Minigun · Миниган | 80 | 24 | ∞ (fast fire · скорострельный) |
| RPG · РПГ | 240 (AoE · по площади) | — | 5 rockets · 5 ракет |

> 🇬🇧
> - **Infinite smoke grenades** `G` — 4 m cloud that blocks bot vision for 16 s
> - **Infinite flashbangs** `F` — boosted, radius **100 meters**, blinds bots up to 7 s, whites out your screen when looking at it
>
> 🇷🇺
> - **Бесконечные смоук-гранаты** `G` — облако радиусом 4 м, блокирует обзор ботам на 16 с
> - **Бесконечные флэшки** `F` — усиленные, радиус **100 метров**, ослепляют ботов до 7 секунд, экран белеет при взгляде на взрыв

### 🏃 Advanced Movement / Продвинутое движение

> 🇬🇧
> - **Crouch** `Shift` — lowers camera to 1 m, slows to 2.5 m/s, works everywhere
> - **DODGE (diagonal run)** — holding `W+A`, `W+D`, `S+A` or `S+D` gives **×1.6 speed** and **full immunity to bot bullets**. DODGE indicator + green edge glow on screen.
>
> 🇷🇺
> - **Приседание** `Shift` — снижает камеру до 1 м, замедляет до 2.5 м/с, работает везде
> - **DODGE (диагональный бег)** — `W+A`, `W+D`, `S+A` или `S+D` даёт **ускорение ×1.6** и **полную неуязвимость** к пулям ботов. Индикатор DODGE + зелёное свечение по краям экрана.

### 🥚 Easter Eggs / Пасхалки

> 🇬🇧 Each map hides a glowing sphere. Crouch next to it — you get a **minigun** (Dust, Inferno) or **RPG** (Mirage).
>
> 🇷🇺 На каждой карте спрятана светящаяся сфера. Присядьте рядом — получите **миниган** (Пыль, Инферно) или **РПГ** (Мираж).

### 🎨 Graphics / Графика

> 🇬🇧
> - **Realistic** — shadows, fog, PCFSoft shadow maps, pixel ratio ×2
> - **Optimized** — no shadows/fog, pixel ratio ×1, brighter lighting
> - Quality switches dynamically **without restarting**
>
> 🇷🇺
> - **Реалистичное** — тени, туман, PCFSoft shadow maps, pixel ratio ×2
> - **Оптимизированное** — без теней и тумана, pixel ratio ×1, ярче освещение
> - Качество переключается динамически **без перезапуска**

---

## 📱 Adaptive Design / Адаптивный дизайн

> 🇬🇧 The game is fully **responsive** and adapts to any device:
>
> - **Window resolution** — WebGL canvas auto-stretches via `renderer.setSize()`, `camera.aspect` recalculated on every `resize`
> - **Menus & overlays** — flexbox-centered, mode cards wrap on narrow screens
> - **HUD** — all elements pinned to screen edges (topbar on top, stats on bottom sides), never overlapping
> - **Pixel ratio** — on mobile, `devicePixelRatio` capped at 2 to avoid FPS drops on Retina displays
> - **Readability** — HUD and crosshair sized to remain legible from 320 px to 4K
> - **README** — this file is responsive: tables, lists, and code blocks render correctly on GitHub, VS Code, Obsidian, and mobile browsers

> 🇷🇺 Игра полностью **адаптивна** и подстраивается под любое устройство:
>
> - **Разрешение окна** — WebGL-канвас растягивается через `renderer.setSize()`, `camera.aspect` пересчитывается при каждом `resize`
> - **Меню и оверлеи** — flexbox с центрированием, карточки режимов переносятся на новую строку на узких экранах
> - **HUD** — элементы привязаны к краям экрана (topbar сверху, статы снизу по бокам), не перекрывают друг друга
> - **Пиксель-рейшо** — на мобильных `devicePixelRatio` ограничивается до 2, чтобы избежать падения FPS на Retina-экранах
> - **Читаемость** — размер шрифта HUD и прицела подобран для экранов от 320 px до 4K
> - **README** — этот файл тоже свёрстан адаптивно: таблицы, списки и блоки кода корректно рендерятся на GitHub, в VS Code, в Obsidian и мобильных браузерах

---

## 🎮 Controls / Управление

| Key · Клавиша | English | Русский |
|---|---|---|
| `W A S D` | Movement | Движение |
| `W+A` / `W+D` / `S+A` / `S+D` | **DODGE** — speed + bullet immunity | **DODGE** — ускорение + неуязвимость |
| `Shift` | Crouch | Приседание |
| `Space` | Jump | Прыжок |
| `Mouse` · `Мышь` | Look | Обзор |
| `LMB` · `ЛКМ` | Fire | Огонь |
| `G` | Smoke grenade (∞) | Смоук-граната (∞) |
| `F` | Flashbang (∞, 100 m) | Флэшка (∞, 100 м) |
| `E` | Plant bomb (Normal, T side) | Заложить бомбу («Обычный», вы — T) |

---

## 🛠 Tech Stack / Технический стек

| Component · Компонент | Technology · Технология |
|---|---|
| Rendering · Рендер | [Three.js](https://threejs.org/) r160 (WebGL) |
| Physics · Физика | Custom AABB collision + raycasting for LOS & bullets · Собственная AABB-коллизия + raycasting для LOS и пуль |
| AI · ИИ | Finite state machine: ENGAGE → FLANK → RETREAT → PATROL → BLIND · Конечный автомат: ENGAGE → FLANK → RETREAT → PATROL → BLIND |
| Audio · Звук | Visual FX only (muzzle flashes, tracers, impacts) · Только визуальные эффекты (вспышки, трейсеры, импакты) |
| Dependencies · Зависимости | **0** (only Three.js via CDN · только Three.js из CDN) |
| Build · Сборка | **Not required · Не требуется** — open `index.html` · открывай `index.html` |

---

## 🗂 Structure / Структура
