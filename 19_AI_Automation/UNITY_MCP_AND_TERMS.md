# Unity MCP, AI Gateway и правила агентного доступа — 2026-10-08

**Юридический статус и проверка:** в актуальных [Unity Terms of Service, обновление 30.06.2026](https://unity.com/legal/terms-of-service) §17.2 (ff) и (gg) Unity ограничивает доступ AI/CLI/MCP и несанкционированные интеграции, требуя Authorized Agentic Access или иной явной авторизации. Определение включает Unity-designated gateway и разрешённые клиенты/серверы. Запрещается без специального права automated ingestion Unity Docs/Asset Store для обучения моделей, репликации базы и competitive intelligence.

[Официальное обсуждение с ответом Unity, 01.07.2026](https://discussions.unity.com/t/new-terms-of-service-is-unity-restricting-local-ai-tools-and-ai-training/1724661/6) уточняет, что ИИ для собственных проектов не запрещён как таковой, но неавторизованный доступ к платформе — отдельный вопрос.

## Официальный путь
- [Unity AI Documentation](https://docs.unity.com/en-us/ai) включает инструменты AI Editor и плагины для сторонних агентов, в том числе Codex.
- [AI menu prerequisites](https://docs.unity.com/en-us/engine/6000.5/manual/unity-ai/ai-menu-access): Unity 6000.0.76f1 или 6000.3+, принятые terms, Unity Cloud-linked project.
- [Обзор Unity AI и Gateway](https://gw-prd.hexagon.unity.com/resources/what-is-unity-ai): поддерживает подключение сторонних агентов через авторизованную интеграцию, доступ зависит от тарифа и условий.

## Сторонние MIT кандидаты — лишь для документального исследования
| Решение | Upstream | Лицензия | Технический интерфейс | Статус |
|---|---|---|---|---|
| [CoplayDev MCP for Unity](../Tool_Catalog/coplaydev-unity-mcp.md) | https://github.com/CoplayDev/unity-mcp | MIT (LICENSE прочитан) | Unity package + Python/uv MCP bridge, 50 инструментов по README | Authorization Unity **не подтверждена**, Editor не тестировался |
| [CoderGamester MCP Unity](../Tool_Catalog/codergamester-mcp-unity.md) | https://github.com/CoderGamester/mcp-unity | MIT (LICENSE.md прочитан) | Unity package + Node/WebSocket bridge | Authorization Unity **не подтверждена**, Editor не тестировался |

**Перед установкой**: выяснить разрешённый Unity gateway/authorization конкретной интеграции, выбрать официальную версию и пакет, проверить сетевой порт и аутентификацию. Не открывать локальный MCP в интернет без нужных средств доступа. MIT-лицензия сама по себе **не разрешает** доступ к Unity в обход Unity ToS. Настройка туннеля и тест на ПК — отдельная задача, не выполненная здесь.
