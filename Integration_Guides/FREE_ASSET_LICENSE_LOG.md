# Лицензии и происхождение ассетов — бесплатный checklist

**Дата:** 2026-10-08. Каталог ссылок не хранит тысячи чужих моделей, но для каждой конкретной модели должна оставаться ссылка на первоисточник.

## Шаблон provenance записи для игрового проекта
```yaml
asset_id: props/wooden_barrel_001
provider: Poly Haven | Kenney | Quaternius
asset_name: "конкретное имя"
source_url: "точная страница ассета"
download_url: "точная официальная ссылка, если известна"
license: CC0-1.0
license_url: "доказательство лицензии"
license_verified_at: "YYYY-MM-DD"
price_paid: 0
price_type: FREE | FREE_STANDARD | PAID_BLOCKED
author: "как указано автором"
downloaded_files: ["barrel.fbx","barrel.png"]
format: FBX
unity_editor_version: "6000.x exact"
import_test: NOT_TESTED | PASSED | FAILED
attribution_required: false
notes: "специфические ограничения или настройки"
```

## Вопросы к бесплатной лицензии
- **CC0:** коммерческое применение разрешено, атрибуция не требуется (но поддержка автора приветствуется); индивидуальный пакет проверять у издателя.
- **MIT/Apache/BSD:** код можно использовать при выполнении notice/attribution/redistribution. Это не гарантирует, что все 3D модели в том же репозитории имеют такую же лицензию.
- **Unity Asset Store:** даже при цене FREE лицензия может быть Standard EULA, Extension Asset или Non-standard; отдельно проверить запрет перепродажи/распространения в asset packs.
- **Unity Companion License:** не MIT, права и ограничения для Unity-dependent products следует читать прямо.
- **GPL Blender:** лицензия самого инструмента не распространяет GPL автоматически на созданную художником модель. Чужая модель всё равно под своей лицензией.
- **Без LICENSE:** оставить в каталоге для чтения, НЕ копировать код/ассеты в коммерческую игру, пока не установлено право использования.

## Скрытая плата, которая не пройдёт проверку
- Kenney All-in-1 ($19.95 minimum на странице itch.io): **BLOCKED_PAID**. Бесплатно брать отдельные наборы с kenney.nl.
- Quaternius Source: платное получение полных Unity проектов и Blend файлов, **BLOCKED_PAID**. Бесплатно брать Standard (часть ассетов).
- Poly Haven: оригинальные CC0 ассеты бесплатны, но некоторые удобные подписочные функции/Vault/Bulk доступны за оплату: **не использовать**.
- Облачные модели, генераторы и платные ключи Unity MCP: **BLOCKED_PAID** без гарантированного 0 ₽.

## Первичные ссылки
- https://polyhaven.com/license
- https://kenney.nl/support
- https://quaternius.com/faq.html
- https://www.blender.org/about/license/
- https://unity.com/legal/as-terms
- [Политика проекта](../FREE_ONLY_POLICY.md)
