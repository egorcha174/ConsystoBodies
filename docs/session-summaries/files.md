# Consysto Files — сводка по прошлым сессиям (на 12.10.2026)

Объединены сессии: «Consysto · Files · Файловый менеджер (начало)», «Consysto · Files · Доработки и ролики в README», «Consysto · Files · Релиз, установщик, витрина GitHub», «Consysto · Продвижение · LinkedIn и Pinterest», «Consysto · Продвижение · Публикации в Telegram и оплата через Boosty».

## Что это
Файловый менеджер для Windows 10/11 (форк Files) с предпросмотром CAD-форматов: STEP (движок OCCT), SolidWorks и КОМПАС (помощник cadmpeg), коллекции чертежей. Репозиторий: github.com/egorcha174/ConsystoFiles (ветки main и publish). Локально: `D:\CODES\ConsystoFiles`.

## Сделано
- Переезд с `C:\Consysto` на `D:\CODES` (сборка в `D:\CODES\_build`, кеш в `D:\CODES\_cache`), коммит 0f84f7c62. Предпросмотр STEP в установленной версии исправлен (коллекция больше не запоминает «картинки нет»).
- Выпуск **v1.26.1010.2049**: портативный zip (148 МБ) и установщик `ConsystoFiles-setup_…exe` (NSIS, без прав администратора, в `%LOCALAPPDATA%\Programs`, RU/EN). Скрипты: `build\consysto\Build-ConsystoSetup.ps1`, `build\consysto\setup\ConsystoFiles-setup.nsi`.
- Витрина GitHub: профиль, шапки README, превью ссылок, закрепы. В README (EN/RU) — обложки-ссылки на видеотур (коммит ec01373ff).
- Русский видеоролик опубликован: YouTube https://youtu.be/Eyohi4TW5ZI, Telegram t.me/print3d_lasercut/220, MAX «Будни конструктора», LinkedIn, Boosty. Итоги: `posts/2026-10-09-consysto-files-video-ru/publication-results.md`. Скрипт публикации в MAX исправлен (ждёт загрузку и проверяет пост).

## Открыто
- **Сбой при первом запуске** после свежей установки: 0xC0000374 (повреждение кучи) в 2 из 3 случаев, второй запуск работает. Причина не найдена (возможно, Defender или гонка инициализации).
- Бирка «forked from» на GitHub: снимает только поддержка GitHub; текст обращения — `build/github-brand/detach-fork-request.md`, отправляет Егор.
- Microsoft Store: черновик 9PHQTP7X9C64 в Partner Center отложен.
- Pinterest как вспомогательный канал: нужен бизнес-аккаунт и работа через Claude in Chrome из локальной сессии (из облака доступа нет). Нужны ссылки на ролики, чтобы подготовить доски и тексты пинов.
- Незакоммиченные изменения скриптов публикации и озвучки.
