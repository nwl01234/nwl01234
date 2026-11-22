# Fullstack Developer · TypeScript · React · Hono · PostgreSQL

Собираю внутренние продукты целиком: API, UI, роли, audit, realtime, фоновая обработка.
Главный кейс — **CardOps**: не CRUD, а сервисный контур с транзакциями, очередями и безопасными сессиями.

Сайт-портфолио: https://nwl01234.github.io/portfolio/

## Selected projects

### [CardOps — card lifecycle platform](https://github.com/nwl01234/cardops)

Внутренний учёт карт: React/TypeScript SPA + core Hono API, отдельные
notifications (WebSocket + NATS JetStream + Redis fanout), OCR-сервис на
Tesseract, documents (PDF + MinIO/S3) и outbox-worker.

- refresh rotation с reuse detection, отзыв сессий через Redis, single-use WS ticket;
- Redis rate limit, RBAC + object-level scope, идемпотентные переходы, append-only audit;
- PostgreSQL + Drizzle, transactional outbox, JetStream durable consumer, DLQ + replay;
- PDF-акт по карте с записью в MinIO/S3;
- 22 API + 5 web + 5 notifications + 4 OCR теста, typecheck и production build.

Запуск без Docker: `start-demo.bat` → `admin / admin123`.

### [business-flow-automator](https://github.com/nwl01234/business-flow-automator)

Заявки и остатки: Python/FastAPI + React/TS, JWT-роли, транзакционное списание,
append-only audit, WebSocket после commit, Docker Compose.
12 pytest. Демо: `docker compose up` → `admin / admin123`.

### [node-service](https://github.com/nwl01234/business-flow-automator/tree/main/node-service)

Тот же доменный поток на TypeScript + Hono: login/orders/confirm/cancel/audit,
JWT/RBAC, Zod, идемпотентный confirm, 3 теста на `node:test`.
Не второй backend — доказательство переноса правил между runtime.

### [pulse-crm](https://github.com/nwl01234/pulse-crm)

Fullstack CRM: React 18 + TypeScript SPA, async FastAPI, SQLAlchemy 2.0, Alembic, JWT.

## Stack

TypeScript, React, PostgreSQL, Redis, NATS, Docker, JWT, WebSocket, REST,
Node/Hono, FastAPI, SQLAlchemy 2, Drizzle, Vitest, Playwright, pytest, Alembic,
aiogram 3.

## AI в разработке

Cursor / Claude Code / Codex — ускорение; review и ответственность за мной.

## Контакты

- GitHub: https://github.com/nwl01234
- Портфолио: https://nwl01234.github.io/portfolio/
- Резюме и отклики: hh.ru
