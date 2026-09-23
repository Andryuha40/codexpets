# Create your own character

[Русский](creating-pets.ru.md)

Use an original character you have rights to. This guide does not authorize adapting Tikinson.

1. Prepare full-body artwork with a consistent palette and a silhouette readable in a 192 × 208 px cell.
2. Create a transparent 1536 × 2288 px RGBA atlas: 8 columns and 11 rows. Do not draw grid lines, labels or backgrounds. Keep scale consistent and avoid clipping limbs.
3. Arrange animations as follows. Leave unused cells transparent.

| Row (zero-based) | State | Frames |
| --- | --- | --- |
| 0 | idle / Спокойствие | 6 |
| 1 | running-right / Бег вправо | 8 |
| 2 | running-left / Бег влево | 8 |
| 3 | waving / Приветствие | 4 |
| 4 | jumping / Прыжок | 5 |
| 5 | failed / Неудача | 8 |
| 6 | waiting / Ожидание ответа | 6 |
| 7 | running / Работа над задачей | 6 |
| 8 | review / Проверка результата | 6 |
| 9–10 | look / Направления взгляда | 16 |

The last two rows hold 16 gaze directions in 22.5° steps, starting upwards and proceeding clockwise. Keep body placement stable. Verify gaze direction in the application.

4. Export lossless `spritesheet.webp` with a real alpha channel. A painted checkerboard is not transparency.
5. Create `pet.json` with a unique `id`, `displayName`, `description`, `spriteVersionNumber: 2`, and `spritesheetPath: "spritesheet.webp"`. See `characters/tikinson/pet.json` for structure; do not reuse its author attribution or identifier for your character.
6. Inspect every frame on light and dark backgrounds, motion, cell boundaries, blinking and gaze; then install in Codex. The application controls timing and task-to-emotion mapping, not `pet.json`.
7. Include a license, attribution, RU/EN instructions and checksums. Exclude credentials, private prompts, diagnostic logs and third-party application code.
8. Follow `CONTRIBUTING.md` to propose inclusion. Add a new `catalog.json` entry without changing existing character paths.

This describes the format verified for Tikinson, not guaranteed compatibility with every Codex version. No particular image generator or access to application internals is required.
