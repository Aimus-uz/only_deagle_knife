# Deagle_only 🔫

**Deagle_only** (форк [Warmup_deagle](https://github.com/mihaigsm2003/Warmup_deagle)) — простой плагин для Counter-Strike 2 на базе **CounterStrikeSharp**, который принудительно ограничивает игроков только разрешённым оружием (по умолчанию — Desert Eagle и нож) **на протяжении всего матча**, а не только во время варма.

## ✨ Особенности

- Работает весь матч (старт раунда, спавн, в реальном времени)
- По умолчанию разрешено только **Desert Eagle + нож** — остальное оружие игнорируется сервером
- Если игрок подберёт с земли любое другое оружие (AK, M4, AWP и т.д.) — оно автоматически удаляется в течение секунды, взять его нельзя
- Список разрешённого оружия настраивается через `config.cfg`, без пересборки плагина

## 📋 Требования

- Counter-Strike 2 сервер
- [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp) >= 1.0.348

## 🛠️ Установка

1. Скачай последнюю версию из [Releases](../../releases)
2. Помести файлы (`Warmup_deagle.dll`, `Warmup_deagle.deps.json`, `config.cfg`) в:
   ```
   csgo/addons/counterstrikesharp/plugins/Warmup_deagle/
   ```
   (название папки должно совпадать с именем `.dll` без расширения)
3. Перезапусти сервер
4. Проверь через консоль сервера:
   ```
   css_plugins list
   ```

## ⚙️ Настройка (config.cfg)

Файл `config.cfg` создаётся автоматически при первом запуске, если его нет. Формат:

```
allowed_weapons = weapon_deagle, weapon_knife
```

Примеры:

- Только Deagle (даже нож нельзя):
  ```
  allowed_weapons = weapon_deagle
  ```
- Deagle + нож (по умолчанию):
  ```
  allowed_weapons = weapon_deagle, weapon_knife
  ```

После изменения `config.cfg` перезапусти сервер (или выполни `css_plugins reload Warmup_deagle`, если поддерживается сборкой CounterStrikeSharp).

## 🙏 Благодарности

Основано на [Warmup_deagle](https://github.com/mihaigsm2003/Warmup_deagle) от mihaigsm2003.
