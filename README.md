# Разработчик с AI-усилением: автоматизация бизнес-процессов и внутренние инструменты

Собираю рабочие инструменты для бизнеса: заявки, остатки, роли, аудит,
уведомления, дашборды, Telegram-боты. Использую AI как ускоритель разработки,
но отвечаю за архитектуру, код, тесты и результат.

## Что я делаю лучше всего

- Автоматизация бизнес-процессов: заявки, остатки, уведомления, отчёты (Telegram, Google Sheets, APScheduler)
- CRM и внутренние сервисы: роли и права, JWT, аудит действий, миграции
- Real-time дашборды: React + Chart.js, WebSocket
- Telegram-боты (aiogram 3): приём заказов, отчёты, AI-консультант
- LLM в продуктах, где есть польза: ассистент по базе знаний с цитатами источников, консультант витрины

## Избранные кейсы

### 1. [business-flow-automator](https://github.com/nwl01234/business-flow-automator) — автозаявки и остатки

**Проблема:** заявки приходят в чаты и на почту, остатки живут в Google Sheets,
никто не знает, кто и что списал.

**Сделано:** Telegram-бот и веб-форма → единая база заявок; проверка и списание
остатков; журнал операций; роли (admin/manager/bot); WebSocket-дашборд в реальном
времени; дневные отчёты и алерты по низким остаткам.

**Результат:** заявка → списание → уведомление → запись в журнале без человека-диспетчера.

**Стек:** FastAPI, SQLAlchemy 2, PostgreSQL/SQLite, React + Tailwind + Chart.js, WebSocket, aiogram 3, APScheduler, Docker

**Демо:** локальный запуск одной командой, демо-данные и доступы создаются автоматически (`admin / admin123`) — [инструкция](https://github.com/nwl01234/business-flow-automator#демо-за-2-минуты)

![Дашборд](https://raw.githubusercontent.com/nwl01234/business-flow-automator/main/skrin/1.png)

### 2. [orbit-crm](https://github.com/nwl01234/orbit-crm) — корпоративная CRM с AI-ассистентом

**Проблема:** заявки, клиенты и история общения — в таблицах и головах менеджеров;
нужен контроль: кто, что и когда сделал.

**Сделано:** CRM полного цикла — сделки/заявки, RBAC-роли, JWT, аудит всех
действий, AI-ассистент по внутренним данным (RAG), Telegram-бот, rate-limit.

**Результат:** менеджер видит всю историю по клиенту; руководитель — кто и что
делал; AI-ассистент отвечает по базе, без выхода данных наружу.

**Стек:** FastAPI, SQLAlchemy, Jinja2 + Tailwind + Alpine.js, Telegram-бот

### 3. [autoshop](https://github.com/nwl01234/autoshop) — витрина магазина с AI-консультантом

**Проблема:** показать товары и принять заявку без сайта, хостинга и бэкенда.

**Сделано:** статическая витрина на GitHub Pages (0 ₽ за инфраструктуру) +
Telegram-бот с AI-консультантом: сценарий покупки, журнал продаж через GitHub API.

**Результат:** работает витрина → [nwl01234.github.io/autoshop](https://nwl01234.github.io/autoshop/)

![Витрина](https://raw.githubusercontent.com/nwl01234/autoshop/main/skrin/1.png)

### 4. [rag-docs-bot](https://github.com/nwl01234/rag-docs-bot) — бот-ответчик по базе документов

**Проблема:** HR и IT отвечают на одни и те же вопросы сотрудников каждый день;
облачные чаты на внутренних документах использовать нельзя.

**Сделано:** загрузил `.md`-документы — получил бота: ответы только из базы,
каждый ответ со ссылкой на документ-источник; нет ответа — честно говорит,
не выдумывает; встроенная метрика качества (golden-набор, hit-rate@3).

**Результат:** офлайн, без API-ключей, за 2 минуты под любую компанию.

**Быстрый старт:** `pip install -r requirements.txt && uvicorn app:app --port 8095`

## Как я использую AI в разработке

- **Как ускоритель:** Cursor, Claude Code, Codex — черновики кода, рефакторинг, тесты. Финальная архитектура, код-ревью, тесты и деплой — за мной.
- **В продуктах:** ассистент по базе знаний (RAG с цитатами), AI-консультант магазина, классификация обращений.
- **Без магии:** если AI не улучшает метрику задачи — не тащу его в проект.

## Навыки

![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2-D71F00)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![React](https://img.shields.io/badge/React_18-20232A?logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?logo=tailwindcss&logoColor=white)
![aiogram](https://img.shields.io/badge/aiogram_3-26A5E4?logo=telegram&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![GitHub_Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC)

## Контакты

Telegram и телефон — в резюме на hh.ru. Код выше — открыт, вопросы по любому
кейсу отвечу в отклике или на собеседовании.
