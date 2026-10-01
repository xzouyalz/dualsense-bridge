# DualSense Bridge

[English below](#english)

Играй на DualSense по Bluetooth так, будто он подключён проводом: с HD-вибрацией, адаптивными триггерами и звуком из динамика геймпада.

> **Windows может испугаться установщика — это нормально.**
> Я делаю мост один, и платная подпись кода мне пока не по карману. Поэтому при запуске SmartScreen покажет синее окно «Windows защитила ваш компьютер». Нажми **«Подробнее» → «Выполнить в любом случае»**.
> Пара антивирусов на VirusTotal тоже может отметить установщик: так их эвристика реагирует на любые новые неподписанные программы. Результат проверки: [VirusTotal](https://www.virustotal.com/gui/file/a0d43044c591909e428eacd7608519f0ddc8e166c298491ef80e0c09825264d3). SHA-256 установщика указан в описании релиза.

## Зачем это

По Bluetooth Windows и игры видят DualSense «урезанным»: нет HD-вибрации, нет звука в динамик геймпада, а часть игр вообще не узнаёт его как DualSense. По проводу всё работает, но провод — это провод.

Мост берёт геймпад, подключённый по Bluetooth, и показывает Windows **проводной DualSense**. Игры получают всё, что умеют:

- подсказки с кнопками PlayStation;
- подсветку и обычную вибрацию;
- адаптивные триггеры;
- **HD-вибрацию и звук в динамик геймпада** — в играх, которые их поддерживают на ПК.

## Что нужно

- Windows 10 или 11, 64 бита.
- Bluetooth на компьютере.
- DualSense, подключённый к компьютеру по Bluetooth.
- Интернет при установке: установщик скачает два драйвера.

## Установка

1. Скачай `DualSenseBridge-Setup-1.0.0.exe` из [релизов](https://github.com/xzouyalz/dualsense-bridge/releases/latest) и запусти.
2. Если появится SmartScreen — «Подробнее» → «Выполнить в любом случае».
3. На странице «Параметры» можно включить автозапуск и ярлык на рабочем столе.
4. Установщик сам скачает и поставит драйверы с их официальных страниц (с проверкой SHA-256):
   - [usbip-win2](https://github.com/vadimgrn/usbip-win2) — создаёт виртуальный проводной геймпад;
   - [HidHide](https://github.com/nefarius/HidHide) — прячет Bluetooth-геймпад от игр, чтобы они видели только один.
5. При первой установке Windows попросит перезагрузку — драйверам это нужно.

## Как пользоваться

Мост живёт в трее, у часов. Подключи DualSense по Bluetooth — через пару секунд он станет проводным.

В меню значка:

- геймпады и их заряд (при низком заряде придёт уведомление);
- **«Мост включён»** — сними галку, и геймпад снова будет обычным Bluetooth;
- **«Запускать вместе с Windows»**;
- **«Выключить»**.

**Важно для Steam:** у игр с родной поддержкой DualSense выключи Steam Input (свойства игры → Контроллер), иначе Steam перехватит геймпад и игра не увидит его возможностей.

## Частые вопросы

**Игра видит два геймпада.** Перезагрузи компьютер после установки: HidHide начинает прятать Bluetooth-геймпад только после перезагрузки.

**Нет HD-вибрации или звука в динамике.** Эти функции работают только в играх, которые поддерживают их на ПК. Проверь, что Steam Input для игры выключен.

**Как вернуть обычный Bluetooth?** Сними галку «Мост включён» в меню трея или нажми «Выключить».

**Работает с несколькими геймпадами?** Да, каждый подключённый DualSense станет отдельным проводным.

## Удаление

«Параметры → Приложения → DualSense Bridge → Удалить». Галка «Также удалить драйверы» уберёт и usbip-win2 с HidHide — сними её, если они нужны другим программам.

## Поддержать

Мост бесплатный и таким останется. Если он пригодился — можно угостить меня кофе ☕:

- из России, картой или по СБП: [CloudTips](https://pay.cloudtips.ru/p/49e993e8);
- из других стран, USDT:
  - сеть TRON (TRC-20): `TTAa8vJfLNVm8H8CKJqebjJeudPgbwGjN2`
  - сеть TON: `UQAQcWMYWpIOwQmBH2rhPTHcp0pVWP_-pl1Dkx2FDBNM81zt`

Если нет — просто расскажи о мосте другу.

---

## English

Play on your DualSense over Bluetooth as if it were plugged in: with HD haptics, adaptive triggers and sound from the controller speaker.

> **Windows may get nervous about the installer — that's expected.**
> I build the bridge on my own and can't afford a paid code-signing certificate yet, so SmartScreen will show a blue "Windows protected your PC" window. Click **More info → Run anyway**.
> A couple of antivirus engines on VirusTotal may flag it too: their heuristics react to any new unsigned program. Scan results: [VirusTotal](https://www.virustotal.com/gui/file/a0d43044c591909e428eacd7608519f0ddc8e166c298491ef80e0c09825264d3). The installer's SHA-256 is in the release notes.

### Why

Over Bluetooth, Windows and games get a cut-down DualSense: no HD haptics, no controller speaker, and some games don't recognize it as a DualSense at all. A cable fixes that, but it's a cable.

The bridge takes your Bluetooth DualSense and presents it to Windows as a **wired DualSense**, so games get everything they support: PlayStation button prompts, lightbar and rumble, adaptive triggers, and **HD haptics and the controller speaker** in games that use them on PC.

### Requirements

- Windows 10 or 11, 64-bit.
- Bluetooth on the PC and a DualSense paired over it.
- Internet during setup: it downloads two drivers.

### Setup

1. Download `DualSenseBridge-Setup-1.0.0.exe` from the [releases](https://github.com/xzouyalz/dualsense-bridge/releases/latest) and run it.
2. If SmartScreen appears: More info → Run anyway.
3. On the Options page you can turn on start with Windows and a desktop shortcut.
4. Setup downloads and installs the drivers from their official pages (SHA-256 checked): [usbip-win2](https://github.com/vadimgrn/usbip-win2) for the virtual wired controller and [HidHide](https://github.com/nefarius/HidHide) to hide the Bluetooth one from games.
5. The first install asks for a restart — the drivers need it.

### Usage

The bridge lives in the tray by the clock. Connect your DualSense over Bluetooth and it becomes wired in a couple of seconds. The tray menu shows your controllers and their battery, and has **Bridge on**, **Start with Windows** and **Exit**.

**Steam:** turn Steam Input off for games with native DualSense support, or Steam takes over the controller and the game won't see its features.

### FAQ

**The game sees two controllers.** Restart Windows after setup: HidHide hides the Bluetooth controller only after a restart.

**No HD haptics or speaker sound.** Only games that support them on PC use them. Make sure Steam Input is off for the game.

**Several controllers?** Yes, each connected DualSense becomes its own wired controller.

### Uninstall

Settings → Apps → DualSense Bridge → Uninstall. "Also remove drivers" removes usbip-win2 and HidHide too; untick it if other programs need them.

### Support

The bridge is free and will stay free. If it's useful to you, you can buy me a coffee ☕:

- USDT on TRON (TRC-20): `TTAa8vJfLNVm8H8CKJqebjJeudPgbwGjN2`
- USDT on TON: `UQAQcWMYWpIOwQmBH2rhPTHcp0pVWP_-pl1Dkx2FDBNM81zt`
- from Russia: [CloudTips](https://pay.cloudtips.ru/p/49e993e8)

---

[License](LICENSE.txt) · [Third-party notices](THIRD_PARTY_NOTICES.txt)
