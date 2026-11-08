# CapyRiver

[Product website](https://capyriver.pages.dev/) · [App downloads](https://github.com/capyriver/CapyRiver-Downloads/releases) · [GitHub profile](https://github.com/capyriver)

**AI software developer · 2 years building personal projects**  
Local AI · desktop and mobile software · developer tools · automation

I build useful software around difficult engineering problems: running AI models on real devices, connecting them to tools safely, and turning prototypes into applications people can install and use. My work spans local AI, Windows and Android applications, model integration, MCP services, browser workflows, and developer productivity.

I value clear technical boundaries, reproducible builds, careful handling of user data, and honest measurement. I describe what a model or tool can do, where it can fail, and what has actually been verified.

## What I build

### Local-first AI applications

Desktop assistants and mobile prototypes that bring chat, local inference, model selection, file context, and everyday workflows into one product. I work on the full path from the interface and model setup to portable packaging and device-aware resource use.

### Model integration and evaluation

Practical work with quantized GGUF models, LoRA adapters, local inference engines, pinned model revisions, integrity checks, and evaluation notebooks. I distinguish an upstream base model from a custom adapter, and treat benchmark results as evidence to measure rather than a marketing claim.

### Agent and MCP workflows

Connections between AI applications and external tools or data sources, including MCP services, browser reading, repository context, and local file workflows. I focus on clear permissions, confirmation for consequential actions, and making tool results visible to the user.

### Developer productivity

Tools that help with code generation and review, Python and JSON checks, project context, and repeatable desktop workflows. Automation should make work easier to inspect and recover, not hide what it changed.

## Selected work

- **A local AI desktop workspace** — a Windows application with local model engines, persistent conversations, a model catalog, file and repository context, optional agent tools, and checks around downloads and actions.
- **A cross-device assistant prototype** — Windows and Android experiments focused on bringing a consistent assistant experience to devices with different memory, storage, and compute limits.
- **Model adaptation and evaluation workflows** — LoRA integration, quantized inference, reproducible downloads, and notebook-based tests for comparing model behavior and resource use.
- **Tool-connected AI workflows** — MCP integrations and browser/file workflows designed around explicit access and understandable outcomes.
- **Developer tools and automation** — utilities for code-focused workflows, local validation, and repeatable interaction with desktop software.

## Engineering approach

- Prefer local execution when it fits the task and hardware.
- Make model provenance, runtime requirements, and limitations easy to find.
- Verify downloads and packaged artifacts with hashes where available.
- Keep sensitive credentials out of source code and public repositories.
- Use scoped tool access and confirmation for changes that affect external data.
- Test the actual user flow, not only whether a project compiles.

## Technology

C# and .NET · Python · JavaScript / TypeScript · Windows desktop · Android · local LLM inference · GGUF and LoRA workflows · MCP integrations · browser automation · GitHub

## Current focus

Building and documenting local AI software that is practical on everyday hardware, with multilingual interfaces and a clear account of model quality, privacy boundaries, and performance limits.

---

## Русский

### Обо мне

**Разработчик ИИ-приложений · 2 года работы над личными проектами**  
Локальный ИИ · настольные и мобильные приложения · инструменты разработчика · автоматизация

Создаю прикладные решения вокруг сложных инженерных задач: запуск ИИ-моделей на реальных устройствах, безопасное подключение инструментов и превращение прототипов в приложения, которые можно установить и использовать. Работаю с локальным ИИ, приложениями для Windows и Android, интеграцией моделей, MCP-сервисами, браузерными сценариями и инструментами для разработчиков.

В инженерной работе ценю понятные границы доступа, воспроизводимую сборку, аккуратное обращение с данными и честную проверку результата. Описываю не только возможности модели или инструмента, но и ограничения, возможные ошибки и то, что действительно проверено.

### Чем занимаюсь

#### Локальные ИИ-приложения

Настольные помощники и мобильные прототипы, объединяющие чат, локальный запуск моделей, выбор моделей, контекст файлов и повседневные сценарии. Работаю над всем путём — от интерфейса и подключения модели до переносимой сборки и учёта ресурсов устройства.

#### Интеграция и оценка моделей

Практическая работа с квантованными GGUF-моделями, LoRA-адаптерами, локальными движками, закреплёнными версиями весов, проверкой целостности и блокнотами для оценки. Различаю базовую модель из открытого источника и собственный адаптер; бенчмарки рассматриваю как то, что нужно измерять, а не как рекламное обещание.

#### Агентные сценарии и MCP

Связываю ИИ-приложения с внешними инструментами и источниками данных через MCP, чтение веб-страниц, контекст репозиториев и локальные файловые сценарии. Уделяю внимание понятным разрешениям, подтверждению важных действий и видимому результату работы инструментов.

#### Инструменты для разработчиков

Создаю и настраиваю инструменты для работы с кодом, локальной проверки Python и JSON, контекста проектов и повторяемых сценариев на рабочем столе. Автоматизация должна упрощать проверку и восстановление результата, а не скрывать внесённые изменения.

### Примеры направлений проектов

- **Локальное ИИ-рабочее пространство для Windows** — приложение с локальными движками моделей, сохраняемыми диалогами, каталогом моделей, контекстом файлов и репозиториев, агентскими инструментами и проверками загрузок и действий.
- **Помощник для нескольких устройств** — эксперименты для Windows и Android с единым пользовательским опытом для устройств с разной памятью, накопителем и вычислительной мощностью.
- **Интеграция и оценка моделей** — подключение LoRA, квантованный запуск, воспроизводимая загрузка и тесты в блокнотах для сравнения поведения моделей и расхода ресурсов.
- **ИИ-сценарии с подключёнными инструментами** — интеграции MCP, браузерные и файловые процессы с явным доступом и понятным результатом.
- **Инструменты разработчика и автоматизация** — утилиты для работы с кодом, локальные проверки и повторяемое взаимодействие с настольными приложениями.

### Подход к разработке

- Выбираю локальный запуск, когда это подходит задаче и оборудованию.
- Делаю сведения о происхождении модели, требованиях и ограничениях доступными.
- Проверяю загрузки и сборки контрольными суммами, когда это возможно.
- Не храню секреты доступа в исходном коде и публичных репозиториях.
- Использую ограниченные разрешения и подтверждения для внешних изменений.
- Проверяю пользовательский сценарий, а не только успешную компиляцию.

### Технологии

C# и .NET · Python · JavaScript / TypeScript · приложения для Windows · Android · локальный запуск языковых моделей · GGUF и LoRA · MCP-интеграции · автоматизация браузера · GitHub

### В фокусе сейчас

Разработка и документирование локальных ИИ-приложений для обычных устройств: многоязычный интерфейс, понятные границы приватности и честная оценка качества и скорости моделей.

---

## 简体中文

### 关于我

**AI 软件开发者 · 2 年个人项目开发经验**  
本地 AI · 桌面与移动应用 · 开发者工具 · 自动化

我围绕实际工程问题构建软件：让 AI 模型能够在真实设备上运行，让模型以受控方式使用工具，并把原型打磨成可安装、可使用的应用。工作方向包括本地 AI、Windows 与 Android 应用、模型集成、MCP 服务、浏览器工作流和开发效率工具。

我重视清晰的权限边界、可复现的构建流程、对用户数据的谨慎处理和诚实的验证。我会说明模型或工具的能力、局限、可能失败的情况，以及哪些内容已经实际验证。

### 工作方向

#### 本地 AI 应用

开发桌面助手和移动端原型，将聊天、本地推理、模型选择、文件上下文和日常工作流整合起来。从界面和模型连接到便携式打包与设备资源适配，关注完整的使用路径。

#### 模型集成与评估

实践量化 GGUF 模型、LoRA 适配器、本地推理引擎、固定模型版本、完整性校验和评估笔记本。明确区分上游底座模型与定制适配器，并把基准测试视为需要测量的证据，而不是宣传口号。

#### Agent 与 MCP 工作流

通过 MCP 服务、网页阅读、代码仓库上下文和本地文件流程，将 AI 应用连接到外部工具和数据源。关注权限范围、重要操作前的确认，以及用户可以理解和检查的执行结果。

#### 开发者效率工具

构建代码生成与检查、Python 和 JSON 本地验证、项目上下文及可重复桌面工作流相关工具。自动化应便于检查和恢复，而不是隐藏它所做的更改。

### 项目方向

- **本地 AI 桌面工作空间** — Windows 应用，包含本地模型引擎、持久化对话、模型目录、文件与仓库上下文、可选 Agent 工具，以及下载和操作校验。
- **跨设备助手原型** — 面向 Windows 和 Android 的实验，针对内存、存储和算力不同的设备探索一致的助手体验。
- **模型适配与评估流程** — LoRA 集成、量化推理、可复现下载和笔记本测试，用于比较模型行为和资源消耗。
- **工具连接型 AI 工作流** — MCP 集成、浏览器与文件操作流程，强调明确授权和可理解的结果。
- **开发工具与自动化** — 面向代码工作的实用工具、本地验证以及可重复的桌面软件交互。

### 工程原则

- 在任务和设备允许时优先考虑本地运行。
- 清晰说明模型来源、运行要求和能力边界。
- 条件允许时使用校验和验证下载及构建产物。
- 不把访问凭据写入源代码或公开仓库。
- 对外部数据修改使用最小权限和操作确认。
- 验证真实用户流程，而不只检查项目能否编译。

### 技术方向

C# 与 .NET · Python · JavaScript / TypeScript · Windows 桌面应用 · Android · 本地大模型推理 · GGUF 与 LoRA · MCP 集成 · 浏览器自动化 · GitHub

### 当前关注

构建并记录适用于日常设备的本地 AI 软件，重点关注多语言界面、清晰的隐私边界，以及对模型质量和运行速度的真实评估。

---

### Featured software

#### CapyRiver — local AI for Android and PC

[CapyRiver](https://capyriver.pages.dev/) brings local AI to Android phones and PCs, with an iPhone version planned for the future. It runs language models on the user's device, so after setup, supported conversations can be processed locally without sending prompts to a CapyRiver server. Model setup includes download progress and file integrity checks. CapyRiver is designed for efficient on-device inference, with attention to resource and battery use on mobile devices. Visit the [CapyRiver website](https://capyriver.pages.dev/) for more information. [Releases and downloads](https://github.com/capyriver/CapyRiver-Downloads/releases). We plan frequent updates with improvements and fixes; release timing may vary.

#### NORA — a flexible AI workspace for Windows

[NORA — CapyRiver Edition](https://github.com/capyriver/NORA-CapyRiver) is a Windows workspace for chatting with different local AI models and connecting model engines to one convenient interface. It includes a model catalog, saved conversations, adjustable response settings, file and project context, code helpers, and optional MCP connectors for adding external tools. Users can choose among supported model runtimes and configure the workspace for their computer. NORA is built to bring AI chats, models, files, and tools together in one desktop app.

---

## Русский

### Избранные приложения

#### CapyRiver — локальный ИИ для Android и ПК

[CapyRiver](https://capyriver.pages.dev/) переносит локальный ИИ на Android-телефоны и ПК; версия для iPhone планируется в будущем. Языковые модели запускаются на устройстве пользователя, поэтому после настройки поддерживаемые диалоги могут обрабатываться локально, без отправки запросов на сервер CapyRiver. При настройке отображается ход загрузки и проверяется целостность файла модели. CapyRiver разрабатывается с упором на эффективную работу на устройстве и экономное использование ресурсов и заряда батареи на мобильных устройствах. Подробнее — на [сайте CapyRiver](https://capyriver.pages.dev/). [Релизы и загрузки](https://github.com/capyriver/CapyRiver-Downloads/releases). Мы планируем часто выпускать обновления с улучшениями и исправлениями; интервалы между версиями могут меняться.

#### NORA — гибкое ИИ-пространство для Windows

[NORA — CapyRiver Edition](https://github.com/capyriver/NORA-CapyRiver) — приложение для Windows, в котором можно общаться с разными локальными ИИ-моделями и подключать их через единый удобный интерфейс. В NORA есть каталог моделей, сохранение диалогов, настройки ответов, контекст файлов и проектов, инструменты для работы с кодом и дополнительные MCP-коннекторы для подключения внешних инструментов. Пользователь может выбрать подходящий движок модели и настроить рабочее пространство под свой компьютер. NORA объединяет ИИ-чаты, модели, файлы и инструменты в одном приложении.

---

## 简体中文

### 精选应用

#### CapyRiver — 适用于 Android 和 PC 的本地 AI

[CapyRiver](https://capyriver.pages.dev/) 将本地 AI 带到 Android 手机和 PC，未来还计划推出 iPhone 版本。语言模型在用户自己的设备上运行；完成设置后，受支持的对话可在本地处理，无需将提示发送到 CapyRiver 服务器。模型设置过程会显示下载进度，并验证模型文件的完整性。CapyRiver 注重设备端推理效率，并关注移动设备的资源与电池消耗。更多信息请访问 [CapyRiver 网站](https://capyriver.pages.dev/)。[版本与下载](https://github.com/capyriver/CapyRiver-Downloads/releases)。我们计划较频繁地发布改进和修复更新；具体发布时间可能有所不同。

#### NORA — 灵活的 Windows AI 工作空间

[NORA — CapyRiver Edition](https://github.com/capyriver/NORA-CapyRiver) 是一款 Windows 应用，可通过统一、易用的界面与多种本地 AI 模型对话，并连接不同的模型引擎。它提供模型目录、对话保存、回答参数设置、文件与项目上下文、代码辅助工具，以及用于接入外部工具的可选 MCP 连接器。用户可以选择受支持的模型运行环境，并根据自己的电脑进行配置。NORA 将 AI 对话、模型、文件和工具整合到一个桌面应用中。
