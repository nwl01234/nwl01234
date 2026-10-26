# nwl01234 — Fullstack / AI-разработчик

Проектирую и разрабатываю backend и фронтенд сервисов с интеграцией LLM
(RAG, агенты, дообучение локальных моделей). Python · FastAPI · React + TypeScript ·
SQLAlchemy 2.0 · PostgreSQL · Docker · Telegram Bot API.

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React_18-20232A?logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2.0-D71F00?logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Telegram_Bot_API](https://img.shields.io/badge/Telegram_Bot_API-26A5E4?logo=telegram&logoColor=white)

## Проекты

| Проект | Стек | Что внутри |
|---|---|---|
| [orbit-crm](https://github.com/nwl01234/orbit-crm) | FastAPI, SQLAlchemy, Jinja2, Tailwind, Alpine.js | Корпоративная CRM: RBAC, AI-ассистент (RAG), Telegram-бот, аудит, rate-limit |
| [pulse-crm](https://github.com/nwl01234/pulse-crm) | React 18, TypeScript, Vite, FastAPI, Alembic | Full-stack CRM: SPA + async backend, миграции, bulk-операции, refresh-токены |
| [mini-crm](https://github.com/nwl01234/mini-crm) | FastAPI, SQLAlchemy, aiogram 3 | Компактный CRM MVP: JWT, AI + RAG, бот |
| [business-flow-automator](https://github.com/nwl01234/business-flow-automator) | FastAPI, aiogram 3, APScheduler, Docker, React | Автоматизация заказов: Telegram, Google Sheets, WebSocket-дашборд |
| [autoshop](https://github.com/nwl01234/autoshop) | Python, Telegram, GitHub Pages | Автономный магазин-витрина: 5 разделов, AI-консультант на LLM |
| [cad-copilot](https://github.com/nwl01234/cad-copilot) | Python, FastAPI, DXF, LoRA-пайплайн | Генерация DXF-чертежей по тексту + дообучение intent-модели под заказчика |
| [llm-finetune-studio](https://github.com/nwl01234/llm-finetune-studio) | FastAPI, softmax/QLoRA-тренер, JS-дашборд | Платформа дообучения локальных LLM: живые loss-кривые, job runner |
| [rag-docs-bot](https://github.com/nwl01234/rag-docs-bot) | FastAPI, TF-IDF RAG | Бот-ответчик по базе документов с цитированием источника, офлайн |

## Чем занимаюсь

- Проектирование REST API и схем БД (SQLAlchemy 2.0, Alembic)
- JWT-аутентификация, RBAC, аудит действий
- Интеграция LLM: RAG, OpenAI-совместимый API, локальные модели, дообучение
- Telegram-боты (aiogram 3), автоматизация бизнес-процессов
- CI: GitHub Actions, Docker

## Динамика

<img src="https://github-readme-stats.vercel.app/api?username=nwl01234&show_icons=true&theme=tokyonight&hide_border=false" width="47%" alt="stats"/>
<img src="https://streak-stats.demolab.com?user=nwl01234&theme=tokyonight&hide_border=false" width="47%" alt="streak"/>

## AI-инфраструктура: где реализовано

| Навык | Где реализовано |
|---|---|
| Fine tuning (локальные модели) | llm-finetune-studio (softmax→QLoRA), cad-copilot (finetune.py) |
| Оценка качества LLM (LLM-as-a-judge, golden set) | llm-finetune-studio `app/eval.py`, rag-docs-bot `core/eval.py` |
| RAG | rag-docs-bot (TF-IDF + цитирование), orbit-crm (AI-ассистент) |
| Online/offline метрики + регресс-тестирование | llm-finetune-studio (loss/accuracy по эпохам, run-diff), rag-docs-bot (hit-rate@3 отчёт) |
| A/B-тестирование (offline) | rag-docs-bot (`/api/eval`: синонимы vs plain) |
| Качество данных + авто-разметка (consistency) | cad-copilot `core/qa.py` (honeypots), llm-finetune-studio (conflict-детекция) |
| Data lifecycle (сбор → разметка → обучение → eval) | cad-copilot `core/qa.py: eval_trained_model()` — полный цикл |
| Python, SQL, REST API | backend всех проектов (FastAPI, SQLAlchemy 2.0) |
| React/TypeScript | pulse-crm (SPA), business-flow-automator (дашборд) |
| Telegram Bot API | orbit-crm, mini-crm, business-flow-automator (aiogram 3) |
| CI / деплой | GitHub Actions во всех репо, Docker (business-flow-automator) |
