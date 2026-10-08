# 08. Unity 2D — спрайты, уровни, коллизии, анимация и свет

**Первая редакция:** 2026-10-08 · **Версия источников:** Unity 6.0/6.3 · **Live-тест:** нет.

## Важная развилка
2D-игра в Unity может быть плоской по механике и иметь 3D визуал (2.5D), но обычная 2D Physics и 3D Physics — **разные системы**. Rigidbody2D работает с Collider2D, а Rigidbody с 3D Collider. Не склеивать их как эквивалентные компоненты.

## Полный pipeline 2D проекта по официальному Unity
1. Перспектива: side view/platformer, top-down, isometric и размер видимой области.
2. Визуал: pixel art/HD sprites/вектор/анимация костями — выбрать по времени создания ассетов.
3. Создать 2D project template, зафиксировать пакеты/рендер.
4. Организовать сцены, GameObjects, Prefabs и структуру Assets.
5. Настроить import изображения как `Sprite (2D and UI)`, Pixels per Unit и фильтрацию (для пиксель-арта часто Point, при иных стилях — другое).
6. Создать уровни Tilemap либо вручную размещёнными Prefabs.
7. Добавить SpriteRenderer и анимацию кадров/2D Animation.
8. Добавить Rigidbody2D + Collider2D, слои столкновений, проверить Trigger и collision callbacks.
9. Настроить камеру и размеры/масштабы, UI и управление мышью/сенсором/геймпадом.
10. Добавить аудио и при необходимости URP 2D Renderer с Light 2D.
11. Проверить производительность, ошибки и сборку на реальной платформе.

Первоисточник: [Unity 6.3 2D creation workflow](https://docs.unity.com/en-us/engine/6000.3/manual/unity2d/2d-game-development/2d-game-creation-wokflow), [Unity 2D physics](https://docs.unity.com/en-us/engine/6000.0/manual/unity2d/2d-physics).

## Компоненты физики
| Компонент | Для чего |
|---|---|
| Rigidbody2D | Тело, управляемое физическим движком |
| Circle/Box/Polygon/Capsule Collider2D | Форма столкновений |
| CompositeCollider2D | Сборная форма в подходящем pipeline |
| Trigger 2D | Обнаружение пересечения без физического препятствия |
| Physics Material 2D | Трение и упругость |
| Joint2D | Физическое соединение тел |
| Layer Collision Matrix | Какие слои с какими сталкиваются |

Проверить настройки каждого Collider и Rigidbody2D в Inspector. Предпочитать простые формы коллизии там, где они достаточно точны. Сложную физику не добавлять без измерений.

## Практика: демонстрация попадания по пугалу
```csharp
using UnityEngine;

public sealed class ArrowHit2D : MonoBehaviour
{
    [SerializeField] private int damage = 1;
    private bool used;

    private void OnTriggerEnter2D(Collider2D other)
    {
        if (used) return;
        if (!other.TryGetComponent<TargetHealth>(out var target)) return;

        used = true;
        target.ApplyDamage(damage);
        Destroy(gameObject);
    }
}
```
**Предпосылки:** `TargetHealth` из главы 05 установлен на том же объекте, что Collider2D; для события OnTriggerEnter2D должно быть корректно настроено участие Rigidbody2D и Collider2D (и Trigger). Если здоровье на родительском объекте, понадобится другая стратегия поиска компонента. Этот фрагмент — **пример, не проверенная сцена**.

## 2D URP и освещение
URP поддерживает 2D Renderer и типы Light 2D: Spot, Sprite, Freeform, Global. **2D lighting не равно физически корректному 3D lighting**. Проверять Sprite-Lit материал и совместимость шейдеров. Для простого прототипа освещение может быть полностью лишним.
Источники: [Light 2D introduction](https://docs.unity.com/en-us/engine/6000.3/manual/unity2d/2d-urp/2d-index/lights-2d-intro), [URP rendering](https://docs.unity.com/en-us/engine/6000.3/manual/render-pipelines/universal-render-pipeline/introduction/urp-concepts/rendering-in-universalrp).

## На что смотреть в тесте
- Sprite не размыт из-за неверного import/filter/PPU относительно камеры.
- Глубина сортировки не перемешивает героев, UI и фон.
- Коллизии корректны на высокой скорости снарядов: непрерывное обнаружение/physics cast при необходимости; не приписывать любому Collider автоматическую защиту от tunneling.
- Целевые устройства имеют приемлемый FPS, память, touch hitboxes и scaling.
- После сцены рестарта нет потерянных ссылок/двойных событий.

## Обязательные дальнейшие углубления
Tilemap + rule tiles; 2D Animation/Skeleton; Sprite Atlas; 2D shadow performance; shader/overdraw; камера и пиксельный масштаб; Input System action assets; физические настройки и профайлер; анимация меню.
