# Unity Profile Analyzer — сравнение CPU-профилей и GC

- **Пакет:** `com.unity.performance.profile-analyzer` (официальный Unity Registry package).
- **Стоимость:** released package без отдельной покупки; использование Unity Editor регулируется условиями Unity, дополнительные платные API не требуются.
- **Лицензия:** не объявлять MIT/CC0; смотреть лицензию конкретного установленного пакета до повторного использования кода. В каталоге только собственное описание.
- **Unity 6000.3:** **1.4.0 released** по официальной таблице.
- **Назначение:** анализ нескольких кадров CPU Profiler и сравнение двух наборов профилей; в 1.4 добавлены показатели GC allocations по маркерам и кадрам.
- **Статус:** DOCUMENTED / NOT_RUN; реальные profiler captures в редакторе или Player не снимались.

## Бесплатный рабочий процесс
1. В Unity 6.3 откройте Package Manager и установите `com.unity.performance.profile-analyzer` 1.4.0.
2. В стандартном Profiler запишите одинаковые сценарии на одной платформе: baseline и новая версия (например, генерация карты, толпа NPC, смена сцены).
3. Откройте Window → Analysis → Profile Analyzer, загрузите оба набора и сравните CPU markers, распределение времени и GC allocations.
4. Сохраните результаты с версиями Editor/пакета, платформой и числом кадров. Повторите на Player: Editor overhead может искажать сравнение.
5. При обмене `.pdata` учтите: версия 1.4 использует формат **9**; Profile Analyzer **1.3.4 и ранее не открывает новые .pdata**. Старые файлы версии 7/8 читаются новой версией.

## Ограничения
- Доступность пакета и версии документально подтверждена, установка на компьютере не проверена.
- Анализ CPU/GC не заменяет GPU Profiler и Memory Profiler.
- Для кросс-версийной передачи результатов лучше обмениваться исходными Profiler `.data` файлами.

## Официальные источники (проверено 2026-10-10)
- Unity 6000.3 version matrix: https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-performance-profile-analyzer
- Unity 1.4 upgrade/.pdata compatibility: https://docs.unity.cn/Packages/com.unity.performance.profile-analyzer@1.4/manual/upgrade-guide.html
- Unity 1.4 package manual: https://docs.unity3d.com/Packages/com.unity.performance.profile-analyzer@1.4/manual/index.html
