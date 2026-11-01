# Источник

Форк [mattpocock/skills](https://github.com/mattpocock/skills) для билда [claude-build](https://github.com/nikraman111/claude-build), ветка `build` от коммита `5beb35b` от 19.10.2026, лицензия MIT (см. `LICENSE`).

Изменения относительно оригинала:
- у 10 команд снят запрет на вызов Клодом (`disable-model-invocation`): `wayfinder`, `grill-with-docs`, `to-spec`, `to-tickets`, `implement-spec`, `implement`, `triage`, `retro`, `improve-codebase-architecture`, `setup-matt-pocock-skills`. Владелец запускает их выбором в меню, без копирования команды (claude-build #134). Запрет обойти нельзя: Claude Code блокирует вызов, а `skillOverrides` на скиллы плагинов не действует. Когда запускать команду, решают правила билда;
- версия в `.claude-plugin/plugin.json` — `<версия Мэтта>-build.<номер>`: без новой версии обновление плагина правку не подхватит;
- `grilling` спрашивает по одному через меню, а не пакетом: правило билда не всегда перебивает прямое указание скилла (проба 01.11.2026: 0 меню, список текстом);
- добавлен этот файл.

Намеренно не тронуто: настройки Codex (`agents/openai.yaml`) и деление на команды и скиллы в `skills/engineering/README.md`. Билд идёт только на Claude Code.

Обновление: влить новую версию Мэтта в ветку `build`, проверить этот список, поднять версию, затем новый `sha` в `marketplace.json` билда, проверка и запись в его `CHANGELOG.md`.
