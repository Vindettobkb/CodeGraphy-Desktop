# CodeGraphy v2.1.1
### Visual Context Orchestrator & Context Intelligence Platform for AI-First Developers

&lt;p align=&quot;center&quot;&gt;
  &lt;img src=&quot;https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-blue?style=for-the-badge&amp;logo=windows&quot; alt=&quot;Platform&quot; /&gt;
  &lt;img src=&quot;https://img.shields.io/badge/Architecture-100%25%20Local--First-emerald?style=for-the-badge&quot; alt=&quot;Architecture&quot; /&gt;
  &lt;img src=&quot;https://img.shields.io/badge/Release-v2.1.1-38bdf8?style=for-the-badge&quot; alt=&quot;Release&quot; /&gt;
  &lt;img src=&quot;https://img.shields.io/badge/Protocol-MCP%20(14%20Tools)-cyan?style=for-the-badge&quot; alt=&quot;MCP&quot; /&gt;
  &lt;img src=&quot;https://img.shields.io/badge/Security-Nuitka%20Machine%20C%20%2B%20RC4%20Obfuscated-red?style=for-the-badge&quot; alt=&quot;Security&quot; /&gt;
&lt;/p&gt;

---

## Interactive Showcase / Демонстрация возможностей

&lt;p align=&quot;center&quot;&gt;
  &lt;b&gt;1. Auto-Discovery &amp; Living Architecture Map Generation / Автосканирование и живой граф&lt;/b&gt;&lt;br&gt;
  &lt;i&gt;Scan any local repository to automatically discover modules, extract dependencies, and build a real-time reactive graph.&lt;/i&gt;&lt;br&gt;
  &lt;img src=&quot;https://github.com/user-attachments/assets/115c3574-b887-4214-befb-fdb27c5a76b4&quot; alt=&quot;Scan &amp; Living Graph&quot; width=&quot;850&quot; /&gt;
&lt;/p&gt;

&lt;p align=&quot;center&quot;&gt;
  &lt;b&gt;2. Layer Filtering &amp; 1-Click IDE Deep Linking (PyCharm / VS Code / Cursor) / Фильтрация слоев и переход в IDE&lt;/b&gt;&lt;br&gt;
  &lt;i&gt;Filter domain models, database layers, and jump directly from any architectural node into the exact file and line inside your local IDE in full project context.&lt;/i&gt;&lt;br&gt;
  &lt;img src=&quot;https://github.com/user-attachments/assets/67355e0c-ab08-4b67-898f-ee6171afbc63&quot; alt=&quot;Layer Filtering &amp; IDE Jump&quot; width=&quot;850&quot; /&gt;
&lt;/p&gt;

&lt;p align=&quot;center&quot;&gt;
  &lt;b&gt;3. AI-Powered Architectural Analysis with AST Context / Архитектурный анализ с AST-контекстом&lt;/b&gt;&lt;br&gt;
  &lt;i&gt;Gemini, Claude, and local Ollama models reason over your project using signature-only AST skeletons with zero token waste.&lt;/i&gt;&lt;br&gt;
  &lt;img src=&quot;https://github.com/user-attachments/assets/ca3fc0fe-44fd-4f0a-a64e-5aa5c91e3756&quot; alt=&quot;AI Architecture Reasoning&quot; width=&quot;850&quot; /&gt;
&lt;/p&gt;

---

## Language Select / Выберите язык
- [English](#english)
  - [What Problems Does CodeGraphy Solve?](#what-problems-does-codegraphy-solve)
  - [Download Latest Release (v2.1.1)](#download-latest-release-v211)
  - [Key Architecture & Features](#key-architecture--features)
  - [CodeGraphy Markdown Format (.cg.md)](#codegraphy-markdown-format-cgmd)
- [Русский](#russian--русский)
  - [Какие проблемы решает CodeGraphy?](#какие-проблемы-решает-codegraphy)
  - [Скачать релиз (v2.1.1)](#скачать-релиз-v211)
  - [Главные возможности и архитектура](#главные-возможности-и-архитектура)
  - [Формат CodeGraphy Markdown (.cg.md)](#формат-codegraphy-markdown-cgmd)
- [System Requirements & Checksums](#системные-требования-и-безопасность--system-requirements--security)

---

## English

### What Problems Does CodeGraphy Solve?

Modern AI-assisted development suffers from three major bottlenecks:

1. **Context Window Bloat & Cost:** Copying full implementation code (thousands of lines) into LLMs burns token limits, skyrockets API costs, and dilutes the AI's attention span.
2. **Model Hallucinations & Lost In The Middle:** When given massive files with irrelevant internal helper logic, AI models frequently forget high-level project boundaries, invent invalid imports, or hallucinate non-existent interfaces.
3. **Fragmented Architectural Knowledge:** Codebases are divided across dozens of microservices, modules, and directories. Developers waste hours explaining to ChatGPT or Claude how module A connects to adapter B and database C.

**CodeGraphy resolves all three:** It turns your architecture into an interactive, visual living graph, extracts signature-only AST skeletons across 19 languages, and feeds clean, precise context directly to any AI model or MCP client.

---

### Download Latest Release (v2.1.1)

- **[Download CodeGraphy Setup 2.1.1.exe (139.07 MB)](https://www.google.com/search?q=https://github.com/Vindettobkb/CodeGraphy-Desktop/releases)**
  - **SHA-256:** `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C`
- **[Download CodeGraphy Portable 2.1.1.exe (127.39 MB)](https://www.google.com/search?q=https://github.com/Vindettobkb/CodeGraphy-Desktop/releases)** *(zero installation required)*
  - **SHA-256:** `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F`

---

### Key Architecture & Features

#### 1. Multi-Language Unified IR & AST Context Extraction (82.83% Verified Token Savings)
Instead of sending entire file bodies, the Unified IR engine (Python native `ast` + lazy-loaded Tree-sitter providers across **19 languages**: Python, TypeScript, JavaScript, Go, Rust, Java, Kotlin, Scala, C, C++, C#, PHP, Ruby, Swift, Lua, SQL, Vue, HTML, CSS) strips internal implementation blocks across 5 compression modes (`INTERFACE_ONLY`, `ARCHITECTURE_OVERVIEW`, `FULL_SIGNATURES`, `DEPENDENCY_FOCUS`, `SMART_CONTEXT`) while preserving:
- Function, struct, interface, and class definitions with inheritance trees.
- Exact parameter names, type annotations, decorators, and default values.
- Docstrings, return signatures, and exported symbols.
- **Verified Benchmark (`tiktoken cl100k_base`):** Weighted token savings of **82.83%** in `SMART_CONTEXT` mode while preserving 100% of public contracts, plus automatic secret redaction (`sk-*`, `AIza*`, `ghp_*`, `.env`).

#### 2. Living Multi-Topic Architecture Canvas
- **Obsidian-Style Interactive Canvas:** Powered by React Flow with smooth physics, drag-and-drop node organization, Focus Mode, and status markers (`To do`, `In progress`, `Done`).
- **Multi-Topic Focus & Resizable Drawers:** Pair several independent or interconnected modules simultaneously (`selectedTopicIds`), inspect every included file (`Full | AST | Off`) in the Hybrid Context Inspector, and resize right-hand drawers smoothly.
- **Linear / Graphite Minimalist Palette:** Professional dark-mode design system (`#0b0c0e` / `#121417` / `#1e2227`) with zero visual noise, `Ctrl + K` Command Palette, and 1-click IDE Deep Linking (`vscode://`, `cursor://`, `pycharm://`).

#### 3. Industrial Architecture Analysis with Tarjan O(V+E) Cycle Detection
- **Instant Drift Detection:** Validates layer boundaries via `codegraphy.yaml` and detects cyclical imports in milliseconds (10,000 files scanned cold in ~1.71s, warm incremental cache in ~0.04s).
- **Coupling Metrics:** Calculates Afferent (`Ca`) and Efferent (`Ce`) coupling, `Mean Instability`, flags god modules, and exports architecture reports to **Mermaid.js**, **JSON**, and **HTML**.

#### 4. Integrated AI Chat with 340+ Models & Instant SSE Streaming
- **Native Support:** Google Gemini, OpenAI (`GPT-4o`, `o3`), Anthropic (`Claude`), DeepSeek, Qwen, xAI Grok, OpenRouter.
- **Local Private Models:** Auto-detects running local GPU instances via **Ollama**, **LM Studio**, and **Open WebUI** with 0-latency offline inference.
- **Persistent Local History:** Chat sessions and workspace state are stored locally in `.codegraphy/`, featuring automatic smart-naming and instant session switching.

#### 5. Context Intelligence Platform & Official 14-Tool MCP Server
- **Official Model Context Protocol (MCP) Server:** Runs locally over sandboxed STDIO, exposing **14 validated tools** (`get_architecture_summary`, `get_module_contract`, `query_subgraph`, `build_smart_context`, `analyze_change_impact`, `get_architecture_diff`, `search_symbols`, `get_context_preset`, `save_context_preset`, `record_context_memory`, `run_impacted_tests`, `get_workspace_status`, `plan_change`, `explain_dependency`) to Claude Desktop and Cursor.
- **Change Impact & Blast Radius:** Computes multi-hop upstream dependencies (`Hop 1`, `Hop 2+`) affected by code modifications before committing.
- **Architecture Git Diff & AI Context Memory:** Live visualization of working tree changes compared to `HEAD` overlaid directly onto the canvas, plus ADR memory with user-verified guardrails.

#### 6. Intellectual Property Protection
- **Python-to-Native Machine Code (Nuitka + Zig):** Backend modules are compiled into x86_64 native machine code (`main.exe`) with **no `.pyc` bytecode files**.
- **Cryptographic Frontend Obfuscation (RC4 + Control Flow Flattening):** Production JS bundle hardened with RC4 string encryption, state-machine flattening, and `sourcemap: false`.
- **ASAR Integrity & DevTools Lockdown:** Production binaries enforce bundle integrity and disable DevTools.

---

### CodeGraphy Markdown Format (`.cg.md`)

&lt;details&gt;
&lt;summary&gt;&lt;b&gt;📐 Click to expand `.cg.md` Specification &amp; One-Shot AI Generation Prompt&lt;/b&gt;&lt;/summary&gt;

CodeGraphy introduces an open, declarative Markdown standard for sharing architecture between developers, Git repositories, and AI systems.

#### AI Architecture Generation Prompt
Copy and send this prompt to ChatGPT, Claude, Gemini, or DeepSeek:

```text
Generate a complete software architecture for my project using the CodeGraphy v2.1 Markdown format.
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

&lt;/details&gt;

---

## Russian / Русский

### Какие проблемы решает CodeGraphy?

При разработке с помощью современных нейросетей разработчики постоянно сталкиваются с тремя барьерами:

1. **Переполнение контекста (Context Bloat) и трата токенов:** Копирование исходных файлов целиком быстро сжигает лимиты контекстного окна, делает запросы дорогими и замедляет генерацию.
2. **Галлюцинации нейросетей (Lost in the Middle):** Когда в модель загружают тысячи строк второстепенного вспомогательного кода, нейросеть забывает архитектуру, выдумывает несуществующие импорты и ломает типизацию.
3. **Разрозненность архитектуры:** Реальная фича всегда распределена по разным слоям: роутеры, сервисы, модели БД, очереди. Разработчик вынужден каждый раз вручную собирать контекст и объяснять нейросети, как устроена система.

**CodeGraphy решает эти проблемы:**
Инструмент строит интерактивный архитектурный граф проекта в стиле Obsidian, связывает ноды с реальными файлами на диске, выжимает из кода компактный каркас через AST-парсер (19 языков) и кормит нейросеть или MCP-агента чистым, концентрированным контекстом.

---

### Скачать релиз (v2.1.1)

- **[Скачать инсталлятор CodeGraphy Setup 2.1.1.exe (139.07 МБ)](https://www.google.com/search?q=https://github.com/Vindettobkb/CodeGraphy-Desktop/releases)**
  - **Контрольная сумма SHA-256:** `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C`
- **[Скачать портативную версию CodeGraphy Portable 2.1.1.exe (127.39 МБ)](https://www.google.com/search?q=https://github.com/Vindettobkb/CodeGraphy-Desktop/releases)** *(работает без установки)*
  - **Контрольная сумма SHA-256:** `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F`

---

### Главные возможности и архитектура

#### 1. Мультиязычный Unified IR и умная AST-выжимка (82.83% подтвержденной экономии токенов)
Встроенный движок (нативный Python `ast` + лениво загружаемые Tree-sitter провайдеры для **19 языков**: Python, TypeScript, JavaScript, Go, Rust, Java, Kotlin, Scala, C, C++, C#, PHP, Ruby, Swift, Lua, SQL, Vue, HTML, CSS) поддерживает 5 режимов сжатия (`INTERFACE_ONLY`, `ARCHITECTURE_OVERVIEW`, `FULL_SIGNATURES`, `DEPENDENCY_FOCUS`, `SMART_CONTEXT`), сохраняя классы, наследование, сигнатуры, типы и докстринги.
- **Проверено через `tiktoken (cl100k_base)`:** взвешенная экономия в режиме `SMART_CONTEXT` составляет **82.83%** при 100% сохранении публичных контрактов + автоматическое маскирование секретов (`sk-*`, `AIza*`, `ghp_*`, `.env`).

#### 2. Интерактивный канвас и мульти-контекст (Multi-Topic Context)
- **Живой граф связей:** React Flow с Focus Mode, статусами (`To do`, `In progress`, `Done`), палитрой команд `Ctrl + K` и растягиваемыми шторками чата и анализа.
- **Hybrid Context Inspector & Deep Linking:** Просмотр причины включения каждого файла (`Provenance`), ручной выбор `[ Full | AST | Off ]` и переход в 1 клик прямо на нужную строку в VS Code, Cursor или PyCharm.
- **Дизайн-система Linear / Graphite:** Строгая темная палитра (`#0b0c0e` / `#121417` / `#1e2227`) без визуального шума.

#### 3. Архитектурный анализ на алгоритме Tarjan O(V+E)
- **Мгновенный поиск циклов и нарушений слоев:** Проверка правил `codegraphy.yaml` (холодное сканирование 10 000 файлов за ~1.71 с, инкрементальный кэш за ~0.04 с).
- **Метрики связанности:** Расчет `Ca`, `Ce`, `Mean Instability`, детектирование God-модулей и экспорт в **Mermaid.js**, **JSON** и **HTML**.

#### 4. Встроенный AI-чат на 340+ моделей и локальные модели
- **Провайдеры:** Google Gemini, OpenAI, Anthropic Claude, DeepSeek, Qwen, xAI Grok, OpenRouter + автообнаружение локальных **Ollama**, **LM Studio**, **Open WebUI**.
- **Потоковый вывод (SSE) и локальное хранение:** Диалоги и воркспейс хранятся локально в папке `.codegraphy/`.

#### 5. Платформа контекстного интеллекта и официальный MCP-сервер (14 инструментов)
- **Локальный MCP Server (STDIO):** Песочница с 14 инструментами (`get_architecture_summary`, `get_module_contract`, `query_subgraph`, `build_smart_context`, `analyze_change_impact`, `get_architecture_diff`, `search_symbols`, `get_context_preset`, `save_context_preset`, `record_context_memory`, `run_impacted_tests`, `get_workspace_status`, `plan_change`, `explain_dependency`) для Claude Desktop и Cursor.
- **Анализ радиуса поражения (Blast Radius) и Git Diff:** Отображение затронутых модулей (`Hop 1`, `Hop 2+`) и изменений относительно `HEAD` прямо на графе.

#### 6. Защита от декомпиляции и слива кода
- **Трансляция Python в машинный код (Nuitka + Zig):** Никаких `.pyc` файлов внутри `main.exe` — чистый нативный бинарник `x86_64`.
- **Крипто-обфускация фронтенда (RC4 + CFF) и ASAR:** Шифрование строкового пула, стейт-машины и блокировка DevTools в релизе.

---

### Формат CodeGraphy Markdown (`.cg.md`)

&lt;details&gt;
&lt;summary&gt;&lt;b&gt;📐 Нажмите, чтобы раскрыть синтаксис `.cg.md` и промпт для генерации архитектуры через LLM&lt;/b&gt;&lt;/summary&gt;

#### Готовый промпт для генерации архитектуры через любую нейросеть
Скопируйте и отправьте ChatGPT, Claude, Gemini или DeepSeek:

```text
Спроектируй полную архитектуру моего проекта в формате CodeGraphy v2.1 Markdown.
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

&lt;/details&gt;

---

## Системные требования и безопасность / System Requirements & Security

| Компонент / Component | Требование / Requirement |
| :--- | :--- |
| **Операционная система** | Windows 10 / 11 (64-bit) |
| **Оперативная память (RAM)** | Мин. 4 ГБ (рек. 8 ГБ) |
| **Дисковое пространство** | ~250 МБ свободного места |

---

## Контрольные суммы релизных сборок / Release Checksums

| Файл / File | Версия / Version | Размер / Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- |
| **`CodeGraphy Setup 2.1.1.exe`** | `v2.1.1` | 139.07 MB | `3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C` |
| **`CodeGraphy Portable 2.1.1.exe`** | `v2.1.1` | 127.39 MB | `CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F` |

---

## Контакты и обратная связь / Contacts

- **Telegram:** [@Methyienedloxymethamphetamine](https://t.me/Methyienedloxymethamphetamine)
- **Discord:** `nevindetto`

---

&lt;p align=&quot;center&quot;&gt;
  &lt;b&gt;CodeGraphy — Understand your architecture. Give AI the right context.&lt;/b&gt;
  &lt;br /&gt;
  &lt;sub&gt;Built for developers, designed for AI-first workflows.&lt;/sub&gt;
&lt;/p&gt;
