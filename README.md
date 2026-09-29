# Consysto — Assembly from Bodies

A free add-in for **Autodesk Inventor 2025, 2026 and 2027** that turns a multi-body master part into an assembly of separate parts in one click.

**[Download the installer](https://github.com/egorcha174/ConsystoBodies/releases/latest)** · English and Russian · Windows x64 · no admin rights needed

[Русский ниже](#по-русски)

![A multi-body master part](docs/master.png)

## What it does

Many designers model a whole product inside one part: the housing, the lid, the ribs, all together. Dimensions stay linked, and changing one updates the rest. But production needs separate parts, flat patterns and an assembly.

**Assembly from Bodies** does that step for you:

- every body becomes a separate part, placed in the assembly exactly where it was in the master;
- sheet metal or standard part is chosen from the feature that created the body, so sheet metal parts come out with a working flat pattern; if the type cannot be told, the add-in asks;
- assembly parameters are linked to the master part, iProperties are carried over;
- if the master has several model states (for example a left and a right hand), a separate assembly is built for each checked state, each in its own subfolder;
- before building you choose where the assembly file and the parts go; the choice is remembered in the master part.

![The Create Assembly window](docs/dialog-en.png)

![The resulting assembly](docs/result.png)

A second command, **Refresh Model States**, deals with a quiet Inventor habit: a model state is recomputed only when you activate it. Change the master, and the other states stay out of date until you visit each one. The command activates every state in turn, recomputes and saves it, then updates open parts and assemblies that reference the master.

## Why not the built-in Make Components

Inventor has **Make Components**, and the add-in uses the same mechanism inside — derived parts. The difference is in what is left for you to do by hand: picking a template for each body, making flat patterns, linking parameters, repeating everything for the left and right versions. With five bodies that is fine. With forty sheet metal parts in two hands it is half an hour of the same clicks and a chance to make a mistake in each one.

## Install

1. Save your work and close Inventor.
2. Run `ConsystoBodies-x.y.z-setup.exe` and pick a language.
3. Open a part: the commands are on the **Tools** tab, **Assembly from Bodies** panel.

The installer is not code-signed, so Windows SmartScreen may say it protected your PC. Click **More info → Run anyway**.

Part templates "Sheet Metal (mm)" and "Standard (mm)" (or Sheet Metal / Standard) must be in the templates folder of the active Inventor project.

**Important:** running Assembly from Bodies again recreates the part files in the chosen folder. Make your changes in the master part, not in the generated parts.

Uninstall: Windows Settings → Apps → Consysto Assembly from Bodies.

## Status

Tested on Inventor 2027. Inventor 2025 and 2026 are supported by the same build but have not been checked yet — if something goes wrong, please open an issue.

Free for personal and commercial use, provided as is, without warranty. The source code is not published. See the [Privacy Notice](PRIVACY.md).

Author: Egor Chayka, design engineer. Telegram channel: [@print3d_lasercut](https://t.me/print3d_lasercut), questions: [@egor_chayka](https://t.me/egor_chayka).

---

## По-русски

Бесплатное дополнение для **Autodesk Inventor 2025, 2026 и 2027**: из многотельной мастер-детали одной кнопкой делает сборку отдельных деталей.

**[Скачать установщик](https://github.com/egorcha174/ConsystoBodies/releases/latest)** · русский и английский интерфейс · Windows x64 · права администратора не нужны

![Окно «Создание сборки»](docs/dialog-ru.png)

- Каждое тело становится отдельной деталью и встаёт в сборку на своё место.
- Листовая или обычная деталь — определяется по операции, которой построено тело; у листовых сразу готова развёртка. Если тип не определился, дополнение спросит.
- Параметры сборки связаны с мастер-деталью, свойства перенесены.
- Если у мастера несколько состояний модели (например, правая и левая версии), для каждого отмеченного делается своя сборка в своей подпапке.
- Перед созданием выбираете, куда положить сборку и детали; выбор запоминается в мастер-детали.

Вторая команда, **«Прокатать состояния»**, по очереди пересчитывает все состояния модели мастер-детали и обновляет открытые сборки и детали, которые на неё ссылаются.

**Установка.** Сохраните работу и закройте Inventor, запустите установщик, выберите язык. Команды — на вкладке «Инструменты» у детали, панель «Сборка из тел». Если Windows скажет, что защитила компьютер, — «Подробнее» → «Выполнить в любом случае»: установщик не подписан сертификатом.

**Важно:** повторная сборка пересоздаёт файлы деталей в выбранной папке. Правки делайте в мастер-детали.

Проверено на Inventor 2027; 2025 и 2026 поддерживаются той же сборкой, но ещё не проверены. Бесплатно для личного и коммерческого использования, без гарантий. Исходный код не публикуется. [Политика конфиденциальности](PRIVACY.md) опубликована на английском языке.

Автор: Егор Чайка, инженер-конструктор. Канал [@print3d_lasercut](https://t.me/print3d_lasercut), вопросы — [@egor_chayka](https://t.me/egor_chayka).
