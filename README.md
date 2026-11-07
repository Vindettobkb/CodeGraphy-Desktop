# ⚡ CodeGraphy
### Visual Context Orchestrator & Living Architecture Graph for AI-First Developers

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-blue?style=for-the-badge&logo=windows" alt="Platform" />
  <img src="https://img.shields.io/badge/Architecture-100%25%20Local--First-emerald?style=for-the-badge" alt="Architecture" />
  <img src="https://img.shields.io/badge/Release-v2.0.0-purple?style=for-the-badge" alt="Release" />
</p>

---

## 🌐 Language Select / Выберите язык
- [English](#-english)
- [Русский](#-русский)

---

## 🇬🇧 English

### What is CodeGraphy?
**CodeGraphy** is a high-performance, local-first developer tool designed to eliminate AI context bloat and reduce model hallucinations.

Instead of manually copying thousands of lines of source code into ChatGPT, Claude, Cursor, or other AI tools, CodeGraphy allows you to visually map your software architecture using an interactive Obsidian-style graph, connect nodes directly to local source files, and extract precise context using Python AST analysis.

### 🚀 Download
👉 **[Download CodeGraphy for Windows (.exe)](#)**

### ✨ Key Features
- **Obsidian-Style Canvas:** Interactive dark graph with fluid physics, floating node dynamics, expandable topic cards, and React Flow integration.
- **Deep AST Extraction:** Removes function and class implementation bodies while preserving signatures, parameters, return types, and docstrings. Can reduce context size by up to 85%.
- **Portable `.cg.md` Architecture Format:** Export and import your entire project architecture, lanes, tasks, dependencies, and file bindings using a single human-readable Markdown file.
- **One-Click IDE Integration:** Open the exact source file and line directly in PyCharm or VS Code.
- **Integrated AI Chat (340+ Models):** A slide-out AI chat supporting OpenAI, Anthropic, Google, DeepSeek, Qwen, xAI, OpenRouter, and automatically detected local models through Ollama and LM Studio.
- **100% Local-First & Private:** No cloud databases. Workspace state is stored locally inside your project's `.archflow/` directory.

---

### 📐 CodeGraphy Markdown Format
CodeGraphy Markdown is an open, declarative format for transferring software architecture between developers and AI models.

#### Why use it?
1. **AI-Powered Architecture Generation:** Ask ChatGPT, Claude, Gemini, DeepSeek, or another LLM to design your project architecture using the CodeGraphy format. Import the generated Markdown file and instantly visualize the architecture.
2. **Git-Friendly & Portable:** Share a single `.md` file instead of complex database exports.
3. **Obsidian-Compatible Links:** Uses familiar `[[Topic Name]]` wiki-links for dependency resolution.
4. **Flexible File Paths:** Supports relative and absolute Windows/Linux paths, automatically recognizing both `/` and `\` separators.

#### 🤖 AI Architecture Generation Prompt
> Copy and send this prompt to any AI model:
> 
> ```text
> Generate a complete software architecture for my project using the CodeGraphy v2.0 Markdown format.
> Follow these requirements:
> - Include YAML frontmatter with format: codegraphy-workspace, version: 2.0, workspace_id, and name.
> - Include three sections: ## Lanes, ## Tasks, and ## Topics.
> - Lanes must use the format: - [lane_id] **Title** | order=0 | color=#38bdf8 | expanded
> - Tasks must use: ### Task: Title `task_id` and include `status`, `lane`, `linked_topics`, and `description`.
> - Topics must use: ### Topic: Title `topic_id` and include `status`, `lane`, `task`, `position`, `description`, `connects_to`, and `files`.
> - Use [[Topic Name]] for connections between topics.
> - File paths must be listed as indented Markdown items under files.
> Generate a complete, valid, import-ready .cg.md document. Do not omit important modules or invent non-existing files. If project files are provided, derive the architecture from their actual contents.
> ```

#### Syntax Example
```markdown
---
format: codegraphy-workspace
version: 2.0
workspace_id: ws_ecommerce_engine
name: E-Commerce Microservices Architecture
---

# Workspace: E-Commerce Microservices Architecture

## Lanes
- [lane_infra] **Infrastructure & Mesh** | order=0 | color=#a855f7 | expanded
- [lane_services] **Core Microservices** | order=1 | color=#38bdf8 | expanded
- [lane_analytics] **Data & Analytics** | order=2 | color=#22c55e | expanded

## Tasks
### Task: Payment Gateway Integration `task_pay_01`
- status: `in_progress`
- lane: `lane_services`
- linked_topics: `topic_order_proc, topic_stripe_adapter`
- description: Implement Stripe webhook handlers and idempotent payment processing.

## Topics
### Topic: Order Processing Service `topic_order_proc`
- status: `in_progress`
- lane: `lane_services`
- task: `task_pay_01`
- position: `(180.0, 200.0)`
- description: Manages customer cart state, order workflows, and checkout pipelines.
- connects_to: [[Stripe Payment Adapter]], [[Event Bus Broker]]
- files:
  - `services/orders/domain/workflows.py`
  - `services/orders/api/checkout_router.py`
  - `services/orders/repositories/cart_repo.py`

### Topic: Stripe Payment Adapter `topic_stripe_adapter`
- status: `done`
- lane: `lane_services`
- task: `task_pay_01`
- position: `(520.0, 200.0)`
- description: Low-level API connector for processing credit cards and refunds.
- connects_to: [[Event Bus Broker]]
- files:
  - `services/payments/adapters/stripe_client.py`
  - `services/payments/schemas/webhooks.py`

### Topic: Event Bus Broker `topic_event_bus`
- status: `done`
- lane: `lane_infra`
- position: `(350.0, 420.0)`
- description: RabbitMQ/Kafka publisher for system-wide asynchronous domain events.
- files:
  - `infrastructure/messaging/publisher.py`
  - `infrastructure/messaging/events/order_events.py`
```

---

## 🇷🇺 Русский

### Что такое CodeGraphy?
**CodeGraphy** — это высокопроизводительный локальный инструмент для разработчиков, предназначенный для решения проблем переполнения контекста (*Context Bloat*) и снижения количества галлюцинаций нейросетей.

Вместо ручного копирования сотен и тысяч строк исходного кода в ChatGPT, Claude, Cursor или другие AI-инструменты, CodeGraphy позволяет визуализировать архитектуру проекта в виде интерактивного графа в стиле Obsidian, связывать узлы с реальными файлами и извлекать компактный контекст с помощью анализа синтаксического дерева Python (AST).

### 🚀 Скачать
👉 **[Скачать установщик CodeGraphy для Windows (.exe)](#)**

### ✨ Главные возможности
- **Интерактивный граф в стиле Obsidian:** Тёмный холст с плавной физикой связей, динамическими узлами, разворачиваемыми карточками и интеграцией React Flow.
- **Умный AST-парсер:** Удаляет тела функций, методов и классов, сохраняя сигнатуры, аргументы, типы возвращаемых значений и докстринги. Позволяет экономить до 85% токенов контекстного окна.
- **Собственный формат `.cg.md`:** Экспортируйте и импортируйте архитектуру проекта, этапы разработки, задачи, связи и привязанные файлы одним Markdown-документом.
- **Мгновенный переход в IDE:** Открывайте нужный файл и конкретную строку прямо в PyCharm или VS Code.
- **Встроенный AI-чат (340+ моделей):** Поддержка OpenAI, Anthropic, Google, DeepSeek, Qwen, xAI, OpenRouter и других провайдеров. Также предусмотрено автоматическое обнаружение локальных моделей через Ollama и LM Studio.
- **Полная конфиденциальность (Local-First):** Никаких облачных баз данных. Состояние рабочего пространства хранится локально в директории `.archflow/` вашего проекта.

---

### 📐 Формат CodeGraphy Markdown
CodeGraphy Markdown — это открытый декларативный формат для переноса архитектуры программных проектов между разработчиками и нейросетями.

#### Зачем нужен этот формат?
1. **Генерация архитектуры через ИИ:** Попросите ChatGPT, Claude, Gemini, DeepSeek или другую нейросеть спроектировать архитектуру вашего проекта по формату CodeGraphy. Импортируйте полученный Markdown-файл и получите готовый интерактивный граф.
2. **Удобное хранение в Git:** Один лёгкий `.md`-файл заменяет сложные экспорты баз данных и легко читается в любом текстовом редакторе.
3. **Совместимость с Obsidian:** Для связей между модулями используются привычные wiki-ссылки `[[Название модуля]]`.
4. **Гибкая работа с путями:** Поддерживаются относительные и абсолютные пути Windows/Linux. Разделители `/` и `\` распознаются автоматически.

#### 🤖 Готовый промпт для генерации архитектуры
> Скопируйте и отправьте любой нейросети:
> 
> ```text
> Спроектируй полную архитектуру моего проекта в формате CodeGraphy v2.0 Markdown.
> Соблюдай следующие требования:
> - Используй YAML-шапку с полями format: codegraphy-workspace, version: 2.0, workspace_id и name.
> - Добавь три обязательные секции: ## Lanes, ## Tasks и ## Topics.
> - Для этапов используй формат: - [lane_id] **Название** | order=0 | color=#38bdf8 | expanded
> - Для задач используй: ### Task: Название `task_id` и поля `status`, `lane`, `linked_topics`, `description`.
> - Для модулей используй: ### Topic: Название `topic_id` и поля `status`, `lane`, `task`, `position`, `description`, `connects_to` и `files`.
> - Для связей между модулями используй формат [[Название модуля]].
> - Пути к файлам указывай отдельными элементами Markdown со стандартным отступом в два пробела внутри files.
> Результат должен представлять собой полный, корректный и готовый к импорту документ .cg.md. Не пропускай важные модули и не выдумывай несуществующие файлы. Если предоставлен исходный код проекта, строй архитектуру на основе его реального содержимого.
> ```

#### Пример синтаксиса
```markdown
---
format: codegraphy-workspace
version: 2.0
workspace_id: ws_smart_home
name: Smart Home IoT Platform
---

# Workspace: Smart Home IoT Platform

## Lanes
- [lane_drivers] **Device Drivers & Protocol** | order=0 | color=#f59e0b | expanded
- [lane_core] **Automation Engine** | order=1 | color=#38bdf8 | expanded
- [lane_api] **REST & WebSockets** | order=2 | color=#22c55e | expanded

## Tasks
### Task: Интеграция Zigbee-устройств `task_zigbee_01`
- status: `in_progress`
- lane: `lane_drivers`
- linked_topics: `topic_zigbee_handler, topic_device_state`
- description: Парсинг MQTT-пакетов от датчиков и обновление стейта в памяти.

### Task: Движок правил и сценариев `task_rules_02`
- status: `done`
- lane: `lane_core`
- linked_topics: `topic_rule_engine, topic_device_state`
- description: Создание триггеров для обработки событий автоматизации.

## Topics
### Topic: Обработчик Zigbee MQTT `topic_zigbee_handler`
- status: `in_progress`
- lane: `lane_drivers`
- task: `task_zigbee_01`
- position: `(150.0, 150.0)`
- description: Подписка на MQTT топики Zigbee2MQTT, дешифровка payloads датчиков.
- connects_to: [[Менеджер Состояний Устройств]]
- files:
  - `drivers/zigbee/mqtt_listener.py`
  - `drivers/zigbee/decoders/climate_sensor.py`
  - `drivers/zigbee/decoders/motion_detector.py`

### Topic: Менеджер Состояний Устройств `topic_device_state`
- status: `done`
- lane: `lane_core`
- task: `task_zigbee_01`
- position: `(480.0, 150.0)`
- description: Центральный кэш текущих параметров (температура, статус реле, освещенность).
- connects_to: [[Движок Правил Автоматизации]]
- files:
  - `core/state/device_manager.py`
  - `core/state/cache_store.py`

### Topic: Движок Правил Автоматизации `topic_rule_engine`
- status: `done`
- lane: `lane_core`
- task: `task_rules_02`
- position: `(480.0, 360.0)`
- description: Выполнение условных операторов IF/THEN на основе поступивших метрик.
- files:
  - `core/rules/evaluator.py`
  - `core/rules/actions/notifications.py`
```

---

## 💻 System Requirements / Системные требования

| Component | Requirement |
| :--- | :--- |
| **Operating System** | Windows 10 / 11 (64-bit) |
| **RAM** | Minimum 4 GB |
| **Disk Space** | Approximately 250 MB |

---

## 🛡️ Security & VirusTotal

You can independently check the application files using VirusTotal.  
*Вы можете самостоятельно проверить файлы программы через VirusTotal.*

> **Note:** The application is built without a paid EV code-signing certificate. As a result, some antivirus engines may report heuristic false positives. Always review the scan results yourself.

### SHA-256 Checksums

| File | SHA-256 | VirusTotal |
| :--- | :--- | :--- |
| `CodeGraphy_Setup.exe` | `9b5c5cca9f33718789baac5eacfa7633d44ae7f3d33926e7112b49381a64777a` | [View scan](#) |
| `CodeGraphy.exe` | `1061eefb7dd635c3d55c2c890f497853b0217a39a3f95f9fb2c827a78a38123c` | [View scan](#) |

---

## 💬 Feedback & Contact / Контакты

Have ideas, feature requests, or bug reports? Feel free to get in touch.  
*Есть идеи, предложения по улучшению или нашли ошибку? Свяжитесь напрямую:*

- **Discord:** `nevindetto` (DM / Add as friend)
- **Telegram:** [@Methyienedloxymethamphetamine](https://t.me/Methyienedloxymethamphetamine)
- **GitHub Issues:** [Report a bug / Open an issue](#)

---

<p align="center">
  <b>CodeGraphy — Understand your architecture. Give AI the right context.</b>
  <br />
  <sub>Built for developers, designed for AI-first workflows.</sub>
</p>
