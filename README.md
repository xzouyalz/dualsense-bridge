# DualSense Bridge

[English below](#english)

Беспроводной DualSense на ПК со всеми возможностями: HD-вибрацией, адаптивными триггерами и динамиком.

> **Про предупреждение Windows**
>
> Установщик не подписан: сертификат для подписи стоит денег, а проект я делаю один и бесплатно. Поэтому при первом запуске Windows покажет синее окно «Windows защитила ваш компьютер». Нажми **«Подробнее»**, затем **«Выполнить в любом случае»**.
>
> По той же причине несколько антивирусов на VirusTotal реагируют на файл: они настороженно относятся к любым новым программам без подписи. [Результаты проверки](https://www.virustotal.com/gui/file/a0d43044c591909e428eacd7608519f0ddc8e166c298491ef80e0c09825264d3). Контрольная сумма SHA-256 — в описании релиза.

## Зачем это нужно

Когда DualSense подключён к ПК по Bluetooth, игры не могут использовать его полностью: нет HD-вибрации, не работает динамик, а некоторые игры вообще не распознают геймпад. По проводу всё работает, но играть с кабелем неудобно.

DualSense Bridge решает эту проблему: для Windows и игр Bluetooth-геймпад выглядит так, будто подключён по USB. В итоге работают:

- подсказки с кнопками PlayStation;
- подсветка и вибрация;
- адаптивные триггеры;
- HD-вибрация и динамик геймпада — в играх, которые поддерживают их на ПК.

## Что понадобится

- Windows 10 или 11 (64-бит).
- Bluetooth на компьютере и подключённый к нему DualSense.
- Интернет во время установки: установщик скачает два драйвера.

## Установка

1. Скачай `DualSenseBridge-Setup-1.0.0.exe` со [страницы релизов](https://github.com/xzouyalz/dualsense-bridge/releases/latest) и запусти.
2. Если появится окно SmartScreen — «Подробнее» → «Выполнить в любом случае».
3. В разделе «Параметры» выбери, нужны ли автозапуск и ярлык на рабочем столе.
4. Установщик скачает с GitHub и установит два драйвера, проверив их контрольные суммы:
   - [usbip-win2](https://github.com/vadimgrn/usbip-win2) — создаёт виртуальный проводной геймпад;
   - [HidHide](https://github.com/nefarius/HidHide) — скрывает Bluetooth-геймпад от игр, чтобы они не видели его дважды.
5. В конце понадобится перезагрузка — она нужна драйверам.

## Как пользоваться

После запуска значок моста появится в трее рядом с часами. Подключи DualSense по Bluetooth — через пару секунд игры будут видеть его как проводной.

В меню значка можно:

- посмотреть подключённые геймпады и их заряд (при низком заряде придёт уведомление);
- временно выключить мост — снять галку «Мост включён»;
- включить или выключить автозапуск;
- закрыть программу.

**Если играешь через Steam:** для игр со встроенной поддержкой DualSense отключи Steam Input (Свойства игры → Контроллер). Иначе Steam перехватит геймпад, и игра не получит доступ к его функциям.

## Вопросы и проблемы

**Игра видит два геймпада.** Перезагрузи компьютер: HidHide начинает скрывать Bluetooth-геймпад только после перезагрузки.

**Нет HD-вибрации или звука из динамика.** Эти функции поддерживают не все игры на ПК. Также проверь, что Steam Input для игры отключён.

**Можно подключить несколько геймпадов?** Да, каждый будет работать как отдельный проводной.

## Удаление

Параметры Windows → Приложения → DualSense Bridge → Удалить. Если оставить галку «Также удалить драйверы», вместе с мостом удалятся usbip-win2 и HidHide. Сними её, если они нужны другим программам.

## Поддержать проект

DualSense Bridge бесплатный и останется бесплатным. Если программа пригодилась, буду рад поддержке:

- из России, картой или по СБП: [CloudTips](https://pay.cloudtips.ru/p/49e993e8);
- из других стран, USDT:
  - сеть TRON (TRC-20): `TTAa8vJfLNVm8H8CKJqebjJeudPgbwGjN2`
  - сеть TON: `UQAQcWMYWpIOwQmBH2rhPTHcp0pVWP_-pl1Dkx2FDBNM81zt`

А можно просто рассказать о мосте друзьям — это тоже помогает.

---

## English

A wireless DualSense on PC with everything it can do: HD haptics, adaptive triggers and the built-in speaker.

> **About the Windows warning**
>
> The installer isn't signed: code-signing certificates cost money, and this is a free project I work on alone. So on first launch Windows will show a blue "Windows protected your PC" window. Click **More info**, then **Run anyway**.
>
> For the same reason, a few antivirus engines on VirusTotal flag the file: they're wary of any new unsigned program. [Scan results](https://www.virustotal.com/gui/file/a0d43044c591909e428eacd7608519f0ddc8e166c298491ef80e0c09825264d3). The SHA-256 checksum is in the release notes.

### Why you need it

With a DualSense connected over Bluetooth, games can't use it fully: no HD haptics, no speaker, and some games don't recognize the controller at all. A cable fixes this, but playing tethered isn't much fun.

DualSense Bridge makes your Bluetooth controller look like a USB one to Windows and games. As a result, you get:

- PlayStation button prompts;
- lightbar and rumble;
- adaptive triggers;
- HD haptics and the controller speaker in games that support them on PC.

### Requirements

- Windows 10 or 11 (64-bit).
- Bluetooth on your PC and a DualSense paired to it.
- An internet connection during setup: it downloads two drivers.

### Installation

1. Download `DualSenseBridge-Setup-1.0.0.exe` from the [releases page](https://github.com/xzouyalz/dualsense-bridge/releases/latest) and run it.
2. If SmartScreen appears, click More info → Run anyway.
3. On the Options page, choose whether you want start with Windows and a desktop shortcut.
4. Setup downloads two drivers from GitHub, verifies their checksums and installs them:
   - [usbip-win2](https://github.com/vadimgrn/usbip-win2) creates the virtual wired controller;
   - [HidHide](https://github.com/nefarius/HidHide) hides the Bluetooth controller from games so they don't see it twice.
5. A restart is needed at the end — the drivers require it.

### Usage

Once running, the bridge icon appears in the system tray next to the clock. Connect your DualSense over Bluetooth, and within a couple of seconds games will see it as wired.

From the tray menu you can:

- see connected controllers and their battery level (you'll get a notification when it's low);
- turn the bridge off for a while by unchecking "Bridge on";
- turn start with Windows on or off;
- exit the program.

**If you play through Steam:** turn off Steam Input for games with native DualSense support (game Properties → Controller). Otherwise Steam takes over the controller and the game can't use its features.

### Troubleshooting

**The game sees two controllers.** Restart your PC: HidHide only starts hiding the Bluetooth controller after a restart.

**No HD haptics or speaker sound.** Not every PC game supports these features. Also make sure Steam Input is off for the game.

**Can I use several controllers?** Yes, each one works as a separate wired controller.

### Uninstalling

Windows Settings → Apps → DualSense Bridge → Uninstall. With "Also remove drivers" checked, usbip-win2 and HidHide are removed along with the bridge. Uncheck it if other programs need them.

### Support the project

DualSense Bridge is free and will stay free. If you find it useful, I'd appreciate your support:

- USDT on TRON (TRC-20): `TTAa8vJfLNVm8H8CKJqebjJeudPgbwGjN2`
- USDT on TON: `UQAQcWMYWpIOwQmBH2rhPTHcp0pVWP_-pl1Dkx2FDBNM81zt`
- from Russia: [CloudTips](https://pay.cloudtips.ru/p/49e993e8)

Or just tell your friends about it — that helps too.

---

[License](LICENSE.txt) · [Third-party notices](THIRD_PARTY_NOTICES.txt)
