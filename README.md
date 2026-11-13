 <div align="center">

# CodeGraphy v2.1.1
### Visual Context Orchestrator & Context Intelligence Platform for AI-First Developers

![Windows 10/11 x64](https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-blue?style=for-the-badge&logo=windows)
![Local First](https://img.shields.io/badge/Architecture-100%25%20Local--First-emerald?style=for-the-badge)
![Release](https://img.shields.io/badge/Release-v2.1.1-38bdf8?style=for-the-badge)
![MCP](https://img.shields.io/badge/Protocol-MCP%20(14%20Tools)-cyan?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-Nuitka%20%2B%20RC4-red?style=for-the-badge)

**Understand your architecture. Give AI the right context.**

</div>

---

## 📑 Table of Contents / Содержание

### 🇬🇧 English
- [Feature Showcase](#en-showcase)
- [Problems CodeGraphy Solves](#en-problems)
- [Download the Latest Release](#en-download)
- [Key Features](#en-features)
- [CodeGraphy Markdown Format (.cg.md)](#en-format)
- [AI Prompt for Architecture Generation](#en-prompt)
- [Example .cg.md Document](#en-example)
- [System Requirements](#en-requirements)
- [Release Checksums](#en-checksums)
- [Contacts](#en-contacts)

### 🇷🇺 Русский
- [Демонстрация возможностей](#ru-showcase)
- [Какие проблемы решает CodeGraphy](#ru-problems)
- [Скачать последнюю версию](#ru-download)
- [Основные возможности](#ru-features)
- [Формат CodeGraphy Markdown (.cg.md)](#ru-format)
- [AI-промпт для генерации архитектуры](#ru-prompt)
- [Пример документа .cg.md](#ru-example)
- [Системные требования](#ru-requirements)
- [Контрольные суммы релизов](#ru-checksums)
- [Контакты](#ru-contacts)

---

# 🇬🇧 English

<a id="en-showcase"></a>
# 🎬 Feature Showcase

## 1. Auto-Discovery & Living Architecture Map

Automatically scans repositories, discovers modules, extracts dependencies, and generates a reactive architecture graph.

<p align="center">
  <img src="https://github.com/user-attachments/assets/115c3574-b887-4214-befb-fdb27c5a76b4" alt="Scan and Living Architecture Graph" width="850">
</p>

## 2. Layer Filtering & IDE Deep Linking

Filter architectural layers and jump directly to the corresponding file and line in PyCharm, VS Code, or Cursor.

<p align="center">
  <img src="https://github.com/user-attachments/assets/67355e0c-ab08-4b67-898f-ee6171afbc63" alt="Layer Filtering and IDE Integration" width="850">
</p>

## 3. AI-Powered Architectural Analysis

Gemini, Claude, and local Ollama models analyze architecture using compact AST context.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ca3fc0fe-44fd-4f0a-a64e-5aa5c91e3756" alt="AI Architecture Analysis" width="850">
</p>

---

<a id="en-problems"></a>
# 🧩 Problems CodeGraphy Solves

Modern AI-assisted development faces three major challenges:

### 1. Context Window Bloat

Sending entire source files to LLMs wastes tokens, increases API costs, and reduces the model’s attention to important architectural details.

### 2. AI Hallucinations

Large amounts of irrelevant code make models lose architectural context, causing them to invent interfaces and dependencies that do not exist.

### 3. Fragmented Architectural Knowledge

Real features often span multiple modules, services, adapters, and database layers. Developers repeatedly need to explain how everything is connected.

### The Solution

CodeGraphy transforms a codebase into an interactive architecture graph, extracts compact AST representations for **19 programming languages**, and provides structured context to AI models and MCP clients.

---

<a id="en-download"></a>
# 📥 Download the Latest Release

**Current version: `v2.1.1`**

- [📥 Download CodeGraphy Setup 2.1.1.exe](https://github.com/Vindettobkb/CodeGraphy-Desktop/releases/tag/v2.1.1)
- [📦 Download CodeGraphy Portable 2.1.1.exe](https://github.com/Vindettobkb/CodeGraphy-Desktop/releases/tag/v2.1.1)

The Portable version does not require installation. Both links lead to the GitHub v2.1.1 release page, where you can choose the Setup or Portable asset.

---

<a id="en-features"></a>
# ⚙️ Key Features

## 1. Multi-Language Unified IR & AST Extraction

### Supports 19 languages

Python, TypeScript, JavaScript, Go, Rust, Java, Kotlin, Scala, C, C++, C#, PHP, Ruby, Swift, Lua, SQL, Vue, HTML, CSS.

### Five context compression modes

- `INTERFACE_ONLY`
- `ARCHITECTURE_OVERVIEW`
- `FULL_SIGNATURES`
- `DEPENDENCY_FOCUS`
- `SMART_CONTEXT`

### Preserves

- Function, class, struct, and interface definitions.
- Inheritance relationships.
- Parameter names and type annotations.
- Decorators and default values.
- Docstrings and exported symbols.

**Benchmark:** Claimed token savings of **82.83%** in `SMART_CONTEXT` mode, according to the project benchmark using `tiktoken cl100k_base`.

Automatic redaction is also included for recognized secret patterns such as `sk-*`, `AIza*`, `ghp_*`, and `.env` content.

## 2. Living Multi-Topic Architecture Canvas

Interactive architecture graph powered by React Flow.

- Drag-and-drop node organization.
- Focus Mode.
- Task statuses: `To do`, `In progress`, `Done`.
- Multi-topic selection via `selectedTopicIds`.
- Resizable context and analysis drawers.
- Hybrid Context Inspector with `Full / AST / Off` modes.
- `Ctrl + K` command palette.
- IDE deep linking for VS Code, Cursor, and PyCharm.

## 3. Industrial Architecture Analysis

Architecture analysis is powered by Tarjan’s strongly connected components algorithm.

### Features

- Circular dependency detection.
- Architecture layer validation through `codegraphy.yaml`.
- Afferent Coupling (`Ca`).
- Efferent Coupling (`Ce`).
- Mean Instability.
- God Module detection.
- Export reports to Mermaid.js, JSON, and HTML.

### Project benchmarks

| Scenario | Reported time |
|---|---:|
| Cold scan — 10,000 files | ≈ 1.71 seconds |
| Warm incremental cache | ≈ 0.04 seconds |

## 4. Integrated AI Chat

Supports **340+ models** through multiple providers:

- Google Gemini
- OpenAI
- Anthropic Claude
- DeepSeek
- Qwen
- xAI Grok
- OpenRouter

### Local inference integrations

- Ollama
- LM Studio
- Open WebUI

### Additional features

- SSE streaming.
- Persistent local chat history.
- Automatic session naming.
- Workspace state stored in `.codegraphy/`.

## 5. Official MCP Server — 14 Tools

A local Model Context Protocol (MCP) server using sandboxed STDIO transport.

| MCP Tool | Purpose |
|---|---|
| `get_architecture_summary` | Retrieve an architecture overview |
| `get_module_contract` | Inspect module contracts |
| `query_subgraph` | Query architecture subgraphs |
| `build_smart_context` | Build optimized AI context |
| `analyze_change_impact` | Analyze the impact of changes |
| `get_architecture_diff` | Compare architecture changes |
| `search_symbols` | Search code symbols |
| `get_context_preset` | Retrieve context presets |
| `save_context_preset` | Save context presets |
| `record_context_memory` | Record architectural memory |
| `run_impacted_tests` | Run impacted tests |
| `get_workspace_status` | Retrieve workspace status |
| `plan_change` | Plan architectural changes |
| `explain_dependency` | Explain dependencies |

### Integrations

- Claude Desktop
- Cursor

### Additional capabilities

- Multi-hop dependency analysis.
- Blast Radius visualization.
- Git working-tree diff compared with HEAD.
- Architecture Decision Record (ADR) memory.
- User-verified architectural guardrails.

## 6. Intellectual Property Protection

The production build uses multiple layers of protection.

### Native compilation

- Nuitka compilation.
- Zig toolchain.
- Python backend translated into native machine code.
- No standalone `.pyc` bytecode files in the compiled backend.

### Frontend protection

- RC4 string encryption.
- Control Flow Flattening.
- Production sourcemaps disabled.

### Application integrity

- ASAR integrity verification.
- Production bundle checksum verification.
- DevTools lockdown.

---

<a id="en-format"></a>
# 🗂️ CodeGraphy Markdown Format (.cg.md)

CodeGraphy introduces a declarative Markdown format for sharing software architecture among developers, Git repositories, and AI systems.

The document has three main sections:

- **Lanes** — architectural lanes or areas.
- **Tasks** — development tasks.
- **Topics** — modules and their relationships.

Use `[[Topic Name]]` to link topics. File paths must be written as indented Markdown list items.

---

<a id="en-prompt"></a>
# 🤖 AI Prompt for Architecture Generation

Copy the prompt below into ChatGPT, Claude, Gemini, or DeepSeek:

```text
Generate a complete software architecture for my project
using the CodeGraphy v2.1 Markdown format.

Requirements:

- Include YAML frontmatter:
  format: codegraphy-workspace
  version: 2.0
  workspace_id
  name

- Include three sections:
  ## Lanes
  ## Tasks
  ## Topics

- Lanes format:
  - [lane_id] **Title** | order=0 | color=#38bdf8 | expanded

- Tasks format:
  ### Task: Title `task_id`

  Required fields:
  status
  lane
  linked_topics
  description

- Topics format:
  ### Topic: Title `topic_id`

  Required fields:
  status
  lane
  task
  position
  description
  connects_to
  files

- Use [[Topic Name]] for topic connections.
- File paths must be indented Markdown list items.

Generate a complete, valid, import-ready .cg.md document.

Do not omit important modules.
Do not invent non-existing files.

If source code is provided, derive the architecture
from its actual contents.
```

---

<a id="en-example"></a>
# 🧪 Example .cg.md Document

Example: **Smart Home IoT Platform**

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

### Task: Zigbee Integration `task_zigbee_01`

- status: `in_progress`
- lane: `lane_drivers`
- linked_topics: `topic_zigbee_handler, topic_device_state`
- description: Parse MQTT packets and update device state.

## Topics

### Topic: Zigbee MQTT Handler `topic_zigbee_handler`

- status: `in_progress`
- lane: `lane_drivers`
- task: `task_zigbee_01`
- position: `(150.0, 150.0)`
- description: Subscribe to Zigbee2MQTT topics and decode sensor payloads.
- connects_to: [[Device State Manager]]
- files:
  - `drivers/zigbee/mqtt_listener.py`
  - `drivers/zigbee/decoders/climate_sensor.py`
  - `drivers/zigbee/decoders/motion_detector.py`
```

---

<a id="en-requirements"></a>
# 🖥️ System Requirements

| Component | Requirement |
|---|---|
| Operating System | Windows 10 / 11 (64-bit) |
| RAM | 4 GB minimum, 8 GB recommended |
| Disk Space | Approximately 250 MB |
| Architecture | x86_64 |

<a id="en-checksums"></a>
# 🔐 Release Checksums

SHA-256 checksums can be used to verify the integrity of downloaded files.

| File | Version | Size | SHA-256 |
|---|---:|---:|---|
| CodeGraphy Setup 2.1.1.exe | 2.1.1 | 139.07 MB | `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C` |
| CodeGraphy Portable 2.1.1.exe | 2.1.1 | 127.39 MB | `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F` |

## Short checksum table (as in the original block)

| File | Size | SHA-256 |
|---|---:|---|
| Setup 2.1.1.exe | 139.07 MB | `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C` |
| Portable 2.1.1.exe | 127.39 MB | `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F` |

<a id="en-contacts"></a>
# 📬 Contacts

- **Telegram:** [@Methyienedloxymethamphetamine](https://t.me/Methyienedloxymethamphetamine)
- **Discord:** `nevindetto`

---

<div align="center">

**CodeGraphy — Understand your architecture. Give AI the right context.**

*Built for developers. Designed for AI-first workflows.*

</div>

---

# 🇷🇺 Русский

<a id="ru-showcase"></a>
# 🎬 Демонстрация возможностей

## 1. Auto-Discovery & Living Architecture Map

Автоматически сканирует репозитории, обнаруживает модули, извлекает зависимости и генерирует реактивный архитектурный граф.

<p align="center">
  <img src="https://github.com/user-attachments/assets/115c3574-b887-4214-befb-fdb27c5a76b4" alt="Scan and Living Architecture Graph" width="850">
</p>

## 2. Layer Filtering & IDE Deep Linking

Позволяет фильтровать архитектурные слои и переходить непосредственно к соответствующему файлу и строке в PyCharm, VS Code или Cursor.

<p align="center">
  <img src="https://github.com/user-attachments/assets/67355e0c-ab08-4b67-898f-ee6171afbc63" alt="Layer Filtering and IDE Integration" width="850">
</p>

## 3. AI-Powered Architectural Analysis

Gemini, Claude и локальные модели Ollama анализируют архитектуру, используя компактный AST-контекст.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ca3fc0fe-44fd-4f0a-a64e-5aa5c91e3756" alt="AI Architecture Analysis" width="850">
</p>

---

<a id="ru-problems"></a>
# 🧩 Какие проблемы решает CodeGraphy

Современная AI-разработка сталкивается с тремя основными проблемами:

### 1. Переполнение контекстного окна (Context Window Bloat)

Передача целых исходных файлов LLM расходует токены, увеличивает стоимость API и снижает внимание модели к важным архитектурным деталям.

### 2. Галлюцинации AI (AI Hallucinations)

Большие объёмы нерелевантного кода мешают моделям сохранять архитектурный контекст. В результате AI может придумывать несуществующие интерфейсы и зависимости.

### 3. Разрозненные архитектурные знания (Fragmented Architectural Knowledge)

Реальные функции часто охватывают несколько модулей, сервисов, адаптеров и слоёв базы данных. Разработчикам приходится снова и снова объяснять, как всё связано.

### Решение

CodeGraphy преобразует кодовую базу в интерактивный архитектурный граф, извлекает компактные AST-представления для **19 языков программирования** и предоставляет структурированный контекст AI-моделям и MCP-клиентам.

---

<a id="ru-download"></a>
# 📥 Скачать последнюю версию

**Текущая версия: `v2.1.1`**

- [📥 Скачать CodeGraphy Setup 2.1.1.exe](https://github.com/Vindettobkb/CodeGraphy-Desktop/releases/tag/v2.1.1)
- [📦 Скачать CodeGraphy Portable 2.1.1.exe](https://github.com/Vindettobkb/CodeGraphy-Desktop/releases/tag/v2.1.1)

> Portable-версия не требует установки.

> Обе ссылки ведут на страницу релиза GitHub v2.1.1, где можно выбрать Setup или Portable.

---

<a id="ru-features"></a>
# ⚙️ Основные возможности

## 1. Multi-Language Unified IR & AST Extraction

### Поддержка 19 языков

Python, TypeScript, JavaScript, Go, Rust, Java, Kotlin, Scala, C, C++, C#, PHP, Ruby, Swift, Lua, SQL, Vue, HTML, CSS.

### Пять режимов сжатия контекста

- `INTERFACE_ONLY`
- `ARCHITECTURE_OVERVIEW`
- `FULL_SIGNATURES`
- `DEPENDENCY_FOCUS`
- `SMART_CONTEXT`

### Что сохраняется

- Определения функций, классов, структур и интерфейсов.
- Связи наследования.
- Имена параметров и аннотации типов.
- Декораторы и значения по умолчанию.
- Docstrings и экспортируемые символы.

**Benchmark:** заявленная экономия токенов — **82.83%** в режиме `SMART_CONTEXT`, согласно benchmark проекта на `tiktoken cl100k_base`.

Также предусмотрено автоматическое скрытие распознаваемых секретов, например шаблонов `sk-*`, `AIza*`, `ghp_*` и содержимого `.env`.

## 2. Living Multi-Topic Architecture Canvas

Интерактивный архитектурный граф на базе React Flow.

- Drag-and-drop организация узлов.
- Focus Mode.
- Статусы задач: `To do`, `In progress`, `Done`.
- Выбор нескольких тем через `selectedTopicIds`.
- Изменяемые по размеру панели контекста и анализа.
- Hybrid Context Inspector с режимами `Full / AST / Off`.
- Командная палитра `Ctrl + K`.
- IDE Deep Linking для VS Code, Cursor и PyCharm.

## 3. Industrial Architecture Analysis

Архитектурный анализ построен на алгоритме поиска сильно связных компонент Тарьяна (Tarjan's strongly connected components algorithm).

### Возможности

- Обнаружение циклических зависимостей.
- Проверка архитектурных слоёв через `codegraphy.yaml`.
- Afferent Coupling (`Ca`).
- Efferent Coupling (`Ce`).
- Mean Instability.
- Обнаружение God Module.
- Экспорт отчётов в Mermaid.js, JSON и HTML.

### Бенчмарки проекта

| Сценарий | Заявленное время |
|---|---:|
| Cold scan — 10 000 файлов | ≈ 1.71 секунды |
| Warm incremental cache | ≈ 0.04 секунды |

## 4. Integrated AI Chat

Поддержка **340+ моделей** через нескольких провайдеров:

- Google Gemini
- OpenAI
- Anthropic Claude
- DeepSeek
- Qwen
- xAI Grok
- OpenRouter

### Локальные интеграции

- Ollama
- LM Studio
- Open WebUI

### Дополнительные функции

- SSE streaming.
- Постоянная локальная история чатов.
- Автоматическое именование сессий.
- Хранение состояния workspace в `.codegraphy/`.

## 5. Official MCP Server — 14 Tools

Локальный сервер Model Context Protocol (MCP) с изолированным STDIO-транспортом.

| MCP-инструмент | Назначение |
|---|---|
| `get_architecture_summary` | Получить обзор архитектуры |
| `get_module_contract` | Изучить контракты модулей |
| `query_subgraph` | Запросить подграф архитектуры |
| `build_smart_context` | Создать оптимизированный AI-контекст |
| `analyze_change_impact` | Проанализировать влияние изменений |
| `get_architecture_diff` | Сравнить изменения архитектуры |
| `search_symbols` | Искать символы в коде |
| `get_context_preset` | Получить пресет контекста |
| `save_context_preset` | Сохранить пресет контекста |
| `record_context_memory` | Записать архитектурную память |
| `run_impacted_tests` | Запустить затронутые тесты |
| `get_workspace_status` | Получить состояние workspace |
| `plan_change` | Спланировать архитектурные изменения |
| `explain_dependency` | Объяснить зависимости |

### Интеграции

- Claude Desktop
- Cursor

### Дополнительные возможности

- Multi-hop анализ зависимостей.
- Визуализация Blast Radius.
- Git working-tree diff относительно HEAD.
- Память Architecture Decision Record (ADR).
- Архитектурные ограничения (guardrails), проверенные пользователем.

## 6. Intellectual Property Protection

В production-сборке используются несколько уровней защиты.

### Native compilation

- Компиляция через Nuitka.
- Использование Zig toolchain.
- Python backend переводится в native machine code.
- В скомпилированном backend отсутствуют отдельные `.pyc`-файлы байткода.

### Frontend protection

- RC4-шифрование строк.
- Control Flow Flattening.
- Sourcemaps отключены в production.

### Application integrity

- ASAR integrity verification.
- Проверка checksum production bundle.
- DevTools lockdown.

---

<a id="ru-format"></a>
# 🗂️ Формат CodeGraphy Markdown (.cg.md)

CodeGraphy вводит декларативный Markdown-формат для обмена архитектурой ПО между разработчиками, Git-репозиториями и AI-системами.

Документ включает три основные секции:

- **Lanes** — архитектурные направления.
- **Tasks** — задачи разработки.
- **Topics** — модули и связи между ними.

Для связей между темами используется синтаксис `[[Topic Name]]`. Пути файлов указываются вложенными элементами Markdown-списка.

---

<a id="ru-prompt"></a>
# 🤖 AI-промпт для генерации архитектуры

Скопируйте промпт ниже в ChatGPT, Claude, Gemini или DeepSeek, чтобы сгенерировать архитектуру проекта в формате CodeGraphy.

```text
Создай полную архитектуру моего проекта
в формате Markdown CodeGraphy v2.1.

Требования:

- Добавь YAML frontmatter:
  format: codegraphy-workspace
  version: 2.0
  workspace_id
  name

- Добавь три раздела:
  ## Lanes
  ## Tasks
  ## Topics

- Формат Lanes:
  - [lane_id] **Название** | order=0 | color=#38bdf8 | expanded

- Формат Tasks:
  ### Task: Название `task_id`

  Обязательные поля:
  status
  lane
  linked_topics
  description

- Формат Topics:
  ### Topic: Название `topic_id`

  Обязательные поля:
  status
  lane
  task
  position
  description
  connects_to
  files

- Используй [[Название темы]] для связей между темами.
- Пути к файлам указывай вложенными элементами Markdown-списка.

Создай полный, корректный и готовый к импорту документ .cg.md.

Не пропускай важные модули.
Не выдумывай несуществующие файлы.

Если предоставлен исходный код, строй архитектуру
на основе его реального содержимого.
```

---

<a id="ru-example"></a>
# 🧪 Пример документа .cg.md

Пример: **Smart Home IoT Platform**

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

### Task: Zigbee Integration `task_zigbee_01`

- status: `in_progress`
- lane: `lane_drivers`
- linked_topics: `topic_zigbee_handler, topic_device_state`
- description: Parse MQTT packets and update device state.

## Topics

### Topic: Zigbee MQTT Handler `topic_zigbee_handler`

- status: `in_progress`
- lane: `lane_drivers`
- task: `task_zigbee_01`
- position: `(150.0, 150.0)`
- description: Subscribe to Zigbee2MQTT topics and decode sensor payloads.
- connects_to: [[Device State Manager]]
- files:
  - `drivers/zigbee/mqtt_listener.py`
  - `drivers/zigbee/decoders/climate_sensor.py`
  - `drivers/zigbee/decoders/motion_detector.py`
```

---

<a id="ru-requirements"></a>
# 🖥️ Системные требования

| Компонент | Требование |
|---|---|
| Операционная система | Windows 10 / 11 (64-bit) |
| Оперативная память (RAM) | Минимум 4 GB, рекомендуется 8 GB |
| Место на диске | Приблизительно 250 MB |
| Архитектура | x86_64 |

<a id="ru-checksums"></a>
# 🔐 Контрольные суммы релизов

SHA-256 можно использовать для проверки целостности скачанных файлов.

| Файл | Версия | Размер | SHA-256 |
|---|---:|---:|---|
| CodeGraphy Setup 2.1.1.exe | 2.1.1 | 139.07 MB | `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C` |
| CodeGraphy Portable 2.1.1.exe | 2.1.1 | 127.39 MB | `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F` |

## Краткая таблица контрольных сумм

| Файл | Размер | SHA-256 |
|---|---:|---|
| Setup 2.1.1.exe | 139.07 MB | `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C` |
| Portable 2.1.1.exe | 127.39 MB | `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F` |

<a id="ru-contacts"></a>
# 📬 Контакты

- **Telegram:** [@Methyienedloxymethamphetamine](https://t.me/Methyienedloxymethamphetamine)
- **Discord:** `nevindetto`

---

<div align="center">

**CodeGraphy — Понимай архитектуру. Давай AI правильный контекст.**

*Создано для разработчиков. Разработано для AI-first рабочих процессов.*

</div>
