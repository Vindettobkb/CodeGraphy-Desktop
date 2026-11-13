CodeGraphy v2.1.1
Visual Context Orchestrator & Context Intelligence Platform for AI-First Developers

<p align="center">
<img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-blue?style=for-the-badge&logo=windows" alt="Windows 10/11">
<img src="https://img.shields.io/badge/Architecture-100%25%20Local--First-emerald?style=for-the-badge" alt="Local First">
<img src="https://img.shields.io/badge/Release-v2.1.1-38bdf8?style=for-the-badge" alt="Release">
<img src="https://img.shields.io/badge/Protocol-MCP%20(14%20Tools)-cyan?style=for-the-badge" alt="MCP">
<img src="https://img.shields.io/badge/Security-Nuitka%20%2B%20RC4-red?style=for-the-badge" alt="Security">
</p>

<p align="center">
<b>Understand your architecture. Give AI the right context.</b>
</p>

Interactive Showcase / Демонстрация возможностей
1. Auto-Discovery & Living Architecture Map

Automatically scan repositories, discover modules, extract dependencies, and generate a reactive architecture graph.

<p align="center">
<img src="https://github.com/user-attachments/assets/115c3574-b887-4214-befb-fdb27c5a76b4" alt="Scan and Living Architecture Graph" width="850">
</p>

2. Layer Filtering & IDE Deep Linking

Filter architectural layers and jump directly into the corresponding file and line in PyCharm, VS Code, or Cursor.

<p align="center">
<img src="https://github.com/user-attachments/assets/67355e0c-ab08-4b67-898f-ee6171afbc63" alt="Layer Filtering and IDE Integration" width="850">
</p>

3. AI-Powered Architectural Analysis

Gemini, Claude, and local Ollama models analyze your architecture using compact AST context.

<p align="center">
<img src="https://github.com/user-attachments/assets/ca3fc0fe-44fd-4f0a-a64e-5aa5c91e3756" alt="AI Architecture Analysis" width="850">
</p>

Navigation
English
Русский
System Requirements
Release Checksums
Contacts
English
What Problems Does CodeGraphy Solve?

Modern AI-assisted development has three major problems:

Context Window Bloat: Sending entire source files to LLMs wastes tokens, increases API costs, and reduces attention to important architectural details.
AI Hallucinations: Large amounts of irrelevant implementation code make models lose architectural context and invent non-existent interfaces or dependencies.
Fragmented Architectural Knowledge: Real features span multiple modules, services, adapters, and database layers. Developers repeatedly have to explain how everything connects.

CodeGraphy solves these problems.

It transforms your codebase into an interactive architectural graph, extracts compact AST representations across 19 programming languages, and provides structured context to AI models and MCP clients.

Download Latest Release

Version: v2.1.1

Download CodeGraphy Setup 2.1.1.exe

Download CodeGraphy Portable 2.1.1.exe

The portable version requires no installation.

SHA-256
File	Size	SHA-256
Setup 2.1.1.exe	139.07 MB	3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C
Portable 2.1.1.exe	127.39 MB	CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F
Key Architecture & Features
1. Multi-Language Unified IR & AST Extraction

Supports 19 languages:

Python, TypeScript, JavaScript, Go, Rust, Java, Kotlin, Scala, C, C++, C#, PHP, Ruby, Swift, Lua, SQL, Vue, HTML, CSS.

Five compression modes:

INTERFACE_ONLY
ARCHITECTURE_OVERVIEW
FULL_SIGNATURES
DEPENDENCY_FOCUS
SMART_CONTEXT

Preserves:

Function, class, struct, and interface definitions.
Inheritance relationships.
Parameter names and type annotations.
Decorators and default values.
Docstrings and exported symbols.

Benchmark: 82.83% weighted token savings in SMART_CONTEXT mode, according to the project's tiktoken cl100k_base benchmark.

Includes automatic secret redaction for recognized patterns such as sk-*, AIza*, ghp_*, and .env.

2. Living Multi-Topic Architecture Canvas
Interactive architecture graph powered by React Flow.
Drag-and-drop node organization.
Focus Mode.
Task statuses: To do, In progress, Done.
Multi-topic selection through selectedTopicIds.
Resizable context and analysis drawers.
Hybrid Context Inspector with Full / AST / Off modes.
Ctrl + K command palette.
IDE deep linking for VS Code, Cursor, and PyCharm.
3. Industrial Architecture Analysis

Powered by Tarjan's strongly connected components algorithm.

Features:

Circular dependency detection.
Architecture layer validation through codegraphy.yaml.
Afferent coupling (Ca).
Efferent coupling (Ce).
Mean Instability.
God Module detection.
Mermaid.js, JSON, and HTML report exports.

Project benchmarks:

10,000 files cold scan: approximately 1.71 seconds.
Warm incremental cache: approximately 0.04 seconds.
4. Integrated AI Chat

Supports 340+ models through multiple providers:

Google Gemini
OpenAI
Anthropic Claude
DeepSeek
Qwen
xAI Grok
OpenRouter

Local inference integrations:

Ollama
LM Studio
Open WebUI

Additional features:

SSE streaming.
Persistent local chat history.
Automatic session naming.
Workspace state storage in .codegraphy/.
5. Official MCP Server — 14 Tools

Local Model Context Protocol server using sandboxed STDIO transport.

Available tools:

Tool	Purpose
get_architecture_summary	Retrieve architecture overview
get_module_contract	Inspect module contracts
query_subgraph	Query architecture subgraphs
build_smart_context	Build optimized AI context
analyze_change_impact	Analyze change impact
get_architecture_diff	Compare architecture changes
search_symbols	Search code symbols
get_context_preset	Retrieve context presets
save_context_preset	Save context presets
record_context_memory	Record architectural memory
run_impacted_tests	Run impacted tests
get_workspace_status	Retrieve workspace status
plan_change	Plan architectural changes
explain_dependency	Explain dependencies

Integrations include Claude Desktop and Cursor.

Additional capabilities:

Multi-hop dependency analysis.
Blast radius visualization.
Git working-tree diff compared with HEAD.
Architecture Decision Record (ADR) memory.
User-verified architectural guardrails.
6. Intellectual Property Protection

The production build uses multiple protection layers:

Native compilation

Nuitka compilation.
Zig toolchain.
Python backend translated into native machine code.
No standalone .pyc bytecode files in the compiled backend.

Frontend protection

RC4 string encryption.
Control Flow Flattening.
Disabled production sourcemaps.

Application integrity

ASAR integrity verification.
Production bundle checksum verification.
DevTools lockdown.
CodeGraphy Markdown Format (.cg.md)

CodeGraphy introduces a declarative Markdown format for sharing software architecture between developers, Git repositories, and AI systems.

AI Architecture Generation Prompt

Copy this prompt into ChatGPT, Claude, Gemini, or DeepSeek:

text
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

Example .cg.md Document
markdown
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

Русский
Какие проблемы решает CodeGraphy?

Современная AI-разработка сталкивается с тремя основными проблемами:

Переполнение контекста: Передача целых файлов нейросетям расходует токены, увеличивает стоимость API и снижает качество анализа.
Галлюцинации нейросетей: Избыточный код мешает моделям понимать архитектуру, из-за чего появляются выдуманные импорты и интерфейсы.
Разрозненность архитектуры: Реальные функции распределены между сервисами, адаптерами, моделями БД и другими слоями.

CodeGraphy превращает архитектуру проекта в интерактивный граф, извлекает компактный AST-контекст для 19 языков программирования и передаёт структурированные данные AI-моделям и MCP-агентам.

Скачать последнюю версию

Версия v2.1.1

Скачать CodeGraphy Setup 2.1.1.exe
Скачать CodeGraphy Portable 2.1.1.exe

Portable-версия не требует установки.

Основные возможности

1. AST и Unified IR

Поддержка 19 языков программирования.
Пять режимов извлечения контекста.
Сохранение сигнатур, типов, наследования и публичных интерфейсов.
Заявленная экономия токенов 82.83% в SMART_CONTEXT.

2. Интерактивный архитектурный граф

React Flow.
Drag & Drop.
Focus Mode.
Multi-Topic Context.
Hybrid Context Inspector.
Deep Linking в VS Code, Cursor и PyCharm.
Командная палитра Ctrl + K.

3. Архитектурный анализ

Поиск циклических зависимостей.
Tarjan O(V+E).
Анализ Ca, Ce и Mean Instability.
Проверка архитектурных слоёв.
Экспорт Mermaid.js, JSON и HTML.

4. AI Chat

Gemini, OpenAI, Claude, DeepSeek, Qwen, Grok и OpenRouter.
Локальные Ollama, LM Studio и Open WebUI.
SSE Streaming.
Локальная история диалогов.

5. MCP Server — 14 инструментов

Интеграция с Claude Desktop и Cursor.

Возможности:

Архитектурный анализ.
Поиск символов.
Построение контекста.
Анализ влияния изменений.
Git Diff.
Blast Radius.
Запуск затронутых тестов.
ADR Memory.

6. Защита интеллектуальной собственности

Nuitka + Zig.
Нативная компиляция backend.
RC4-обфускация строк.
Control Flow Flattening.
Sourcemap отключён в production.
ASAR Integrity Verification.
Формат CodeGraphy Markdown

Формат .cg.md предназначен для декларативного описания архитектуры проекта.

Документ содержит три основные секции:

Lanes — архитектурные направления.
Tasks — задачи разработки.
Topics — модули и связи между ними.

Для генерации архитектуры можно использовать AI-промпт из английской секции выше.

System Requirements
Component	Requirement
Operating System	Windows 10 / 11 (64-bit)
RAM	4 GB minimum, 8 GB recommended
Disk Space	Approximately 250 MB
Architecture	x86_64
Release Checksums
File	Version	Size	SHA-256
CodeGraphy Setup	2.1.1	139.07 MB	3B8A36A860489E1FBEDCE1BFC4212527445F93342B3ACDA3BC2A7AD1AE59D92C
CodeGraphy Portable	2.1.1	127.39 MB	CB4727CF036A83B3EFF324473BB9CCEE54145007A1D9685983B99A6EB6F6920F
Contacts
Telegram: @Methyienedloxymethamphetamine
Discord: nevindetto

<p align="center">
<b>CodeGraphy — Understand your architecture. Give AI the right context.</b>
<br>
<sub>Built for developers. Designed for AI-first workflows.</sub>
</p>
