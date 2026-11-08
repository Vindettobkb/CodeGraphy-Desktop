# ⚡ CodeGraphy v2.0
### Visual Context Orchestrator & Living Architecture Graph for AI-First Developers

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-blue?style=for-the-badge&logo=windows" alt="Platform" />
  <img src="https://img.shields.io/badge/Architecture-100%25%20Local--First-emerald?style=for-the-badge" alt="Architecture" />
  <img src="https://img.shields.io/badge/Release-v2.0.0-purple?style=for-the-badge" alt="Release" />
  <img src="https://img.shields.io/badge/Security-Nuitka%20Machine%20C%20%2B%20RC4%20Obfuscated-red?style=for-the-badge" alt="Security" />
</p>

---

## 🌐 Language Select / Выберите язык
- [English](#-english)
  - [What Problems Does CodeGraphy Solve?](#-what-problems-does-codegraphy-solve)
  - [Key Architecture & Features](#-key-architecture--features)
  - [CodeGraphy Markdown Format (.cg.md)](#-codegraphy-markdown-format-cgmd)
  - [System Requirements & Security](#-system-requirements--security)
- [Русский](#-русский)
  - [Какие проблемы решает CodeGraphy?](#-какие-проблемы-решает-codegraphy)
  - [Главные возможности и архитектура](#-главные-возможности-и-архитектура)
  - [Формат CodeGraphy Markdown (.cg.md)](#-формат-codegraphy-markdown-cgmd)
  - [Системные требования и безопасность](#-системные-требования-и-безопасность)

---

## 🇬🇧 English

### 💡 What Problems Does CodeGraphy Solve?

Modern AI-assisted development suffers from three major bottlenecks:

1. **Context Window Bloat & Cost:** Copying full implementation code (thousands of lines) into LLMs burns token limits, skyrockets API costs, and dilutes the AI's attention span.
2. **Model Hallucinations & Lost In The Middle:** When given massive files with irrelevant internal helper logic, AI models frequently forget high-level project boundaries, invent invalid imports, or hallucinate non-existent interfaces.
3. **Fragmented Architectural Knowledge:** Codebases are divided across dozens of microservices, modules, and directories. Developers waste hours explaining to ChatGPT or Claude how module A connects to adapter B and database C.

**CodeGraphy resolves all three:** It turns your architecture into an interactive, visual living graph, extracts signature-only AST skeletons without runtime bloat, and feeds clean, precise context directly to any AI model.

---

### 🚀 Download Latest Release (v2.0.0)

- 👉 **[Download CodeGraphy Setup 2.0.0.exe (138 MB)](https://github.com/)**
- **SHA-256 Checksum:** `B6F80896946748AEA1B366B6A9BD9684715F646A6643CDF302111B13AFB77B00`
- **Portable Version:** Available in `win-unpacked` folder (zero installation required).

---

### ✨ Key Architecture & Features

#### 1. Deep Python AST Context Extraction (-85% Token Waste)
Instead of sending entire file bodies, the built-in AST parser strips internal implementation blocks (`pass`, return calculations, loops) while preserving:
- Function and class definitions with inheritance trees.
- Exact parameter names, type annotations, and default values.
- Docstrings, return signatures, and exported symbols.
- **Result:** You can feed an entire 20-file module into an LLM using only ~1,500 tokens instead of 25,000 tokens, eliminating hallucinations.

#### 2. Living Multi-Topic Architecture Canvas
- **Obsidian-Style Interactive Canvas:** Powered by React Flow with smooth physics, drag-and-drop node organization, and status markers (`To do`, `In progress`, `Done`).
- **Multi-Topic Focus:** Pair several independent or interconnected modules simultaneously (`selectedTopicIds`). The chat compiles unified context across all attached files and dependency edges in real time.
- **Linear / Graphite Minimalist Palette:** Professional dark-mode design system (`#111315` / `#15181B` / `#20252A`) with zero visual noise, aligned action controls (`Copy`, `Retry`), and unobtrusive status badges.

#### 3. Integrated AI Chat with 340+ Models & Instant SSE Streaming
- **Native Support:** Google Gemini (`3.6 Flash`, `3.8 Flash`, `Pro`), OpenAI (`GPT-4o`, `o3`), Anthropic (`Claude 3.5 Sonnet`, `Opus`), DeepSeek, Qwen, xAI Grok, OpenRouter.
- **Local Private Models:** Auto-detects running local GPU instances via **Ollama**, **LM Studio**, and **Open WebUI** with 0-latency offline inference.
- **Sub-Second Streaming:** Server-Sent Events (SSE) stream tokens chunk-by-chunk with intelligent fallback mechanisms (e.g. automatic failover if a cloud model cluster experiences peak-demand spikes).
- **Persistent Local History:** Chat sessions are stored locally in your workspace (`localStorage` / `.archflow`), featuring automatic smart-naming from the initial query and instant session switching.

#### 4. Military-Grade Intellectual Property Protection
CodeGraphy is built with strict multi-layer defense against reverse engineering and decompilation:
- **Python-to-Native Machine Code (Nuitka + Zig):** Backend modules are translated to C source code and compiled directly into an x86_64 binary (`main.exe`) using `zig.exe 0.16.0`. There are **no `.pyc` bytecode files**—decompilers only see raw processor machine instructions (`mov`, `jmp`, `call`).
- **Cryptographic Frontend Obfuscation (RC4 + Control Flow Flattening):** The React 19 codebase is hardened with RC4 string encryption, function flattening into state machines, and dead-code injection.
- **ASAR Integrity & DevTools Lockdown:** Production binaries enforce cryptographically verified bundle checksums preventing binary tampering.

---

### 📐 CodeGraphy Markdown Format (`.cg.md`)

CodeGraphy introduces an open, declarative Markdown standard for sharing architecture between developers, Git repositories, and AI systems.

#### 🤖 AI Architecture Generation Prompt
Copy and send this prompt to ChatGPT, Claude, Gemini, or DeepSeek:

```text
Generate a complete software architecture for my project using the CodeGraphy v2.0 Markdown format.
Follow these requirements:
- Include YAML frontmatter with format: codegraphy-workspace, version: 2.0, workspace_id, and name.
- Include three sections: ## Lanes, ## Tasks, and ## Topics.
- Lanes must use the format: - [lane_id] **Title** | order=0 | color=#38bdf8 | expanded
- Tasks must use: ### Task: Title `task_id` and include `status`, `lane`, `linked_topics`, and `description`.
- Topics must use: ### Topic: Title `topic_id` and include `status`, `lane`, `task`, `position`, `description`, `connects_to`, and `files`.
- Use [[Topic Name]] for connections between topics.
- File paths must be listed as indented Markdown items under files.
Generate a complete, valid, import-ready .cg.md document. Do not omit important modules or invent non-existing files. If project files are provided, derive the architecture from their actual contents.
```

---

## 🇷🇺 Русский

### 💡 Какие проблемы решает CodeGraphy?

При разработке с помощью современных нейросетей разработчики постоянно сталкиваются с тремя барьерами:

1. **Переполнение контекста (Context Bloat) и трата токенов:** Копирование исходных файлов целиком быстро сжигает лимиты контекстного окна, делает запросы дорогими и замедляет генерацию.
2. **Галлюцинации нейросетей (Lost in the Middle):** Когда в модель загружают тысячи строк второстепенного вспомогательного кода, нейросеть «забывает» архитектуру, выдумывает несуществующие импорты и ломает типизацию.
3. **Разрозненность архитектуры:** Реальная фича всегда распределена по разным слоям: роутеры, сервисы, модели БД, очереди. Разработчик вынужден каждый раз вручную собирать контекст и объяснять нейросети, как устроена система.

**CodeGraphy решает эти проблемы:**
Инструмент строит интерактивный архитектурный граф проекта в стиле Obsidian, связывает ноды с реальными файлами на диске, выжимает из кода компактный каркас через синтаксический анализ AST и кормит нейросеть чистым, концентрированным контекстом.

---

### 🚀 Скачать релиз (v2.0.0)

- 👉 **[Скачать инсталлятор CodeGraphy Setup 2.0.0.exe (138 МБ)](https://github.com/)**
- **Контрольная сумма SHA-256:** `B6F80896946748AEA1B366B6A9BD9684715F646A6643CDF302111B13AFB77B00`
- **Портативная версия:** Папка `win-unpacked` (работает сразу без установки).

---

### ✨ Главные возможности и архитектура

#### 1. Умная AST-выжимка контекста (экономия до 85% токенов)
Встроенный парсер анализирует абстрактное синтаксическое дерево Python, вырезая внутреннюю реализацию функций и методов (`pass`, циклы, вспомогательные вычисления), но сохраняя:
- Структуру классов и деревья наследования.
- Точные имена аргументов, type-hints типизацию и дефолтные значения.
- Докстринги и возвращаемые типы.
- **Результат:** 20 файлов сложного сервиса укладываются всего в ~1,500 токенов вместо 25,000, полностью исключая галлюцинации модели.

#### 2. Интерактивный канвас и мульти-контекст (Multi-Topic Context)
- **Живой граф связей:** Построен на базе React Flow с плавной кинематикой, перетаскиванием, связями между модулями и статусами (`To do`, `In progress`, `Done`).
- **Мульти-топики в чате:** Возможность объединять в один AI-контекст сразу несколько связанных модулей. Чат автоматически скомпилирует общий контекст по всем привязанным файлам и смежным связям.
- **Дизайн-система Linear / Graphite:** Элегантный профессиональный интерфейс в глубокой графитовой палитре (`#111315` / `#15181B` / `#20252A`) без визуального шума. Кнопки `Copy` и `Retry` выровнены строго по одной оси.

#### 3. Встроенный AI-чат на 340+ моделей с моментальным стримингом
- **Поддерживаемые провайдеры:** Google Gemini (`3.6 Flash`, `3.8 Flash`, `Pro`), OpenAI (`GPT-4o`, `o3`), Anthropic (`Claude 3.5 Sonnet`, `Opus`), DeepSeek, Qwen, xAI Grok, OpenRouter.
- **Локальные модели без интернета:** Автоматическое обнаружение локальных серверов **Ollama**, **LM Studio**, **Open WebUI** для приватной работы на собственном GPU.
- **Потоковый вывод (SSE):** Первый токен появляется на экране менее чем за 0.5 секунды. Реализован умный авто-фоллбэк (если облачный кластер выбранной модели перегружен, запрос без зависаний переключается на стабильную ревизию).
- **Локальная история сессий:** Диалоги сохраняются в локальном хранилище проекта с автоматическим присвоением названий по первому вопросу и быстрым переключением между ветками.

#### 4. Максимальная защита от декомпиляции и слива кода
CodeGraphy защищён на промышленном уровне:
- **Трансляция Python в машинный Си-код (Nuitka + Zig):** Исходный код бэкенда переводится в язык C и компилируется через `zig.exe 0.16.0` в чистый бинарный машинный код x86_64. Внутри `main.exe` **нет `.pyc` файлов и нет Python-байткода**. При попытке открыть бинарник в IDA Pro или Ghidra взломщик увидит только десятки тысяч строк голого ассемблера (`mov`, `jmp`, `call`).
- **Крипто-обфускация фронтенда (RC4 + CFF):** Весь React 19 интерфейс зашифрован шифром RC4, логика функций разбита на стейт-машины (*Control Flow Flattening*), внедрён мёртвый код (*Dead Code Injection*).
- **Контроль целостности ASAR и блокировка DevTools:** В релизе заблокирована консоль разработчика, а криптографический хеш `asarIntegrity` защищает приложение от подмены ресурсов.

---

### 📐 Формат CodeGraphy Markdown (`.cg.md`)

Архитектура сохраняется в человекочитаемом формате Markdown, совместимом с Git и Obsidian wiki-ссылками `[[Название]]`.

#### 🤖 Готовый промпт для генерации архитектуры через любую нейросеть
Скопируйте и отправьте ChatGPT, Claude, Gemini или DeepSeek:

```text
Спроектируй полную архитектуру моего проекта в формате CodeGraphy v2.0 Markdown.
Соблюдай следующие требования:
- Используй YAML-шапку с полями format: codegraphy-workspace, version: 2.0, workspace_id и name.
- Добавь три обязательные секции: ## Lanes, ## Tasks и ## Topics.
- Для этапов используй формат: - [lane_id] **Название** | order=0 | color=#38bdf8 | expanded
- Для задач используй: ### Task: Название `task_id` и поля `status`, `lane`, `linked_topics`, `description`.
- Для модулей используй: ### Topic: Название `topic_id` и поля `status`, `lane`, `task`, `position`, `description`, `connects_to` и `files`.
- Для связей между модулями используй формат [[Название модуля]].
- Пути к файлам указывай отдельными элементами Markdown со стандартным отступом в два пробела внутри files.
Результат должен представлять собой полный, корректный и готовый к импорту документ .cg.md. Не пропускай важные модули и не выдумывай несуществующие файлы. Если предоставлен исходный код проекта, строй архитектуру на основе его реального содержимого.
```

#### Пример синтаксиса `.cg.md`
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
```

---

## 💻 Системные требования / System Requirements

| Компонент / Component | Требование / Requirement |
| :--- | :--- |
| **Операционная система** | Windows 10 / 11 (64-bit) |
| **Оперативная память (RAM)** | Мин. 4 ГБ (рек. 8 ГБ) |
| **Дисковое пространство** | ~250 МБ свободного места |

---

## 🛡️ Безопасность и контрольные суммы / Security

| Файл / File | Версия / Version | SHA-256 Checksum |
| :--- | :--- | :--- |
| **`CodeGraphy Setup 2.0.0.exe`** | `v2.0.0` | `B6F80896946748AEA1B366B6A9BD9684715F646A6643CDF302111B13AFB77B00` |

---

## 💬 Контакты и обратная связь / Contacts

- **Telegram:** [@Methyienedloxymethamphetamine](https://t.me/Methyienedloxymethamphetamine)
- **Discord:** `nevindetto`

---

<p align="center">
  <b>CodeGraphy — Understand your architecture. Give AI the right context.</b>
  <br />
  <sub>Built for developers, designed for AI-first workflows.</sub>
</p>
