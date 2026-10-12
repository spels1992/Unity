# Реестр доступных плагинов и скиллов для Unity + Blender

**Инвентаризация:** 2026-10-08. Источник: фактически доступные инструменты ChatGPT в беседе и `skills__list`. **Не является проверкой локальных установок, работоспособности или текущей цены каждой внешней услуги.**

## Актуализация 2026-10-12 — навыки для скелетов и анимации

**Актуальный реестр ChatGPT:** [CHATGPT_PLUGINS.md](../CHATGPT_PLUGINS.md). **Подробная производственная инструкция:** [docs/ANIMATION_RIGGING_SKILLS.md](../docs/ANIMATION_RIGGING_SKILLS.md).

- **Scenario Skills — Blender & Unity**: [плагин ChatGPT](https://chatgpt.com/plugins/Plugin_d296061237d0819182131b981a56a216), **17 скиллов**, источник [scenario-labs/skills](https://github.com/scenario-labs/skills) (MIT). Профильные `scenario-blender-rigging`, `scenario-blender-animation`, `scenario-unity-animation`.
- **Блендер+**: [плагин ChatGPT](https://chatgpt.com/plugins/Plugin_7348ae51e6e8819181d0e2a1fed40dd0), **94 скилла**, источник [arjun988/blender-skills](https://github.com/arjun988/blender-skills) (MIT). Профильные `creature-artist` (четвероногие, птицы, монстры), `rigging`, `animation`.
- **Blender MCP и Unity MCP Server подключены**; новые пакеты — справочники Agent Skills, не новые приложения или MCP-серверы. Рабочее выполнение — специализированными MCP, качество проверять живыми тестами.
- **Правило из актуальных PROJECT_INSTRUCTIONS:** Remote Desktop Commander применять **только** для восстановления Windows MCP / WinApp MCP. Раздел инвентаризации ниже сохранён как историческое описание возможностей на 2026-10-08, а не текущие разрешения.

## 1. Рекомендуемые плагины

| Плагин | Где помогает | Когда использовать | Роль | Ограничения / бесплатность |
|---|---|---|---|---|
| **Unity MCP** (48 доступных функций) | Unity сцены, объекты, префабы, C#, анимации, тесты, build, profiler | Работа в подключённом Unity Editor | Основной специализированный | Сначала проверить подключение; `generate_image/model/audio` вызывает BYOK сервисы и **запрещён без доказанного нулевого тарифа** |
| **Unity MCP — blender_bridge** | Blender → Unity: чтение сцены, скриншоты, Python, export GLB/FBX, import и compare | BlenderMCP addon подключён к локальному Blender | Специализированный дополнительный | Без addon/Blender connection не работает; не заменяет полностью Blender API |
| **WIndows MCP** | Управление Blender/Unity через GUI и окна Windows | Когда специализированный инструмент недоступен или для действий в GUI | Резервный | Не считать UI-клики точными тестами; сохранять screenshots/checkpoints |
| **Remote Desktop Commander** | Локальные файлы, терминал/скрипты, диагностика, запуск доступных утилит | Пакетная обработка, Blender Python, проверка установок/проектов | Резервный/вспомогательный | Сначала проверить подключение и лимит; это не обязательно бесплатный независимый продукт |
| **GitHub** | Unity/GameLibrary, карточки, issues, история, коммиты | После каждой законченной исследовательской/инженерной задачи | Постоянный каталог и checkpoint | GitHub/Actions/LFS имеют квоты: избегать платных больших файлов |
| **Context7** | Сверка актуальных API, библиотек, SDK | Перед реализацией/рефакторингом, когда docs могли измениться | Источник документации | Дополнять официальными Unity/Blender источниками; не единственный источник |
| **Figma** | Меню, HUD, UX, дизайн-системы, прототипы UI | Когда нужен графический дизайн/сложный HUD | Опциональный | Использовать только бесплатные доступные возможности, не обязательный для игры |
| **Canva / Adobe Express** | Иконки, промо, обложки, скриншот-композиции | Маркетинговая графика и простой дизайн | Опциональный | У free tier есть ограничения; вместо платных функций Blender/Krita/Inkscape |
| **BrowserAct** (skill/browser automation) | Сбор референсов на динамических сайтах, лицензии/страницы пакетов | Если обычного чтения сайта недостаточно | Опциональный | CLI может требовать отдельную установку; не делать обязательным |
| **GitBook / Google Drive / Notion** | Документация/планы/таблицы | По особому запросу | Необязательный | Главный источник знаний — GitHub Markdown, не платные облачные docs |

**Обновлено 2026-10-12:** отдельный **Blender MCP** присутствует среди подключённых инструментов ChatGPT; состояние живого Blender/аддона/туннеля перепроверять на каждой рабочей сессии.

## 2. Самые полезные скиллы (видны в skills__list)
| Скилл | Практический смысл | Этап |
|---|---|---|
| `superpowers/brainstorming` | Прояснение требований, отбор механик/архитектуры без лишнего scope | Идея и дизайн |
| `superpowers/writing-plans` | Декомпозиция сложной задачи на проверяемые шаги | До разработки |
| `superpowers/using-git-worktrees` | Изолировать экспериментальную ветку/проект | Перед рискованными изменениями |
| `superpowers/subagent-driven-development`, `dispatching-parallel-agents` | Раздать независимые задачи агентам, если такие средства доступны | Большой проект |
| `superpowers/test-driven-development` | Проверка логики C#/компонентов через заранее определённый тест | Реализация систем |
| `superpowers/systematic-debugging` | Не гадать, а находить корневую причину Unity/Blender ошибок | Ошибки |
| `superpowers/verification-before-completion` | Прежде чем утверждать успех, реально проверить console/tests/build/commit | Каждый checkpoint |
| `superpowers/requesting-code-review` | Проверка качества и регрессий | PR/release |
| `figma/figma-use`, `figma-generate-library`, `figma-design-to-code` | UI дизайн → реализация | Только для интерфейсов, если Figma реально нужна |
| `browser-act/browser-act` | Управление динамическими страницами и извлечение информации | Исследование источников |
| `plugin-creator/create-plugin` | Создание повторяемого ChatGPT-плагина для проекта | Только если готовые пути не подходят |
| `google-drive/google-sheets` | Таблицы баланса/времени/ассетов | По запросу, если Markdown недостаточно |

**Обновлено 2026-10-12:** профильные навыки Blender установлены в ChatGPT в двух наборах **Scenario Skills** и **Блендер+**; названия и ссылки приведены выше.

## 3. Рекомендуемый гибкий workflow

```text
Исследование → Unity/Blender docs + Context7 + GitHub
   ↓
Концепция → superpowers/brainstorming → writing-plans
   ↓
3D-модель → Blender Python/bridge (если работает)
   ↓
Игровая сцена → Unity MCP (или безопасный Windows MCP/Editor API fallback)
   ↓
C# и системы → test-driven-development + systematic-debugging
   ↓
Проверка → Unity run_tests + Console + build + screenshot
   ↓
GitHub checkpoint → README/card/issue/commit (verification-before-completion)
```

## 4. Важные оговорки
- «Установлен/доступен в ChatGPT» не гарантирует, что конкретный локальный туннель и Unity/Blender работают прямо сейчас. Это проверяется инструментами при начале задачи.
- Библиотека инструментов ChatGPT предоставляется текущей подпиской и не заменяет бесплатный независимый путь для будущих проектов.
- Не устанавливать и не запускать ничего, что требует платной API key/кредитов. Не вводить реквизиты оплаты.
- Правила Unity AI и авторизованного агентного доступа проверять перед подключением: [UNITY_MCP_AND_TERMS.md](UNITY_MCP_AND_TERMS.md).
- Плагины могут меняться; периодически пересматривать этот список. Не создавать искусственное правило «нет Figma — нет UI».
