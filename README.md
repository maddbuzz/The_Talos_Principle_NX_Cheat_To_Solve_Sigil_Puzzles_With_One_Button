# The Talos Principle NX Cheat To Solve Sigil Puzzles With One Button

<details>
<summary><b>English</b></summary>

An Atmosphere cheat code for Nintendo Switch that solves Sigil (Tetromino) puzzles in *The Talos Principle* by pressing D-Pad Down.

## Description
- The cheat does not implement an independent puzzle solver, but uses the game's **built-in debug functionality**.
- It doesn't solve every puzzle automatically right away, but only when you press the D-Pad Down button.
- **You must have already collected the required sigils for the puzzle.** This cheat only automates the solving process; it does not spawn missing sigils.

## Requirements
- Nintendo Switch with Atmosphere custom firmware
- *The Talos Principle* version **v1.0.2** (Title ID: `010092A00D43C000`, Build ID: `74562DD37142F8EB`)
- EdiZon or Tesla Menu

## Installation
1. Download this repository (green "Code" button → "Download ZIP") and extract it.
2. Copy the `atmosphere` folder to the root of your SD card.
3. If prompted by your OS, agree to merge/replace folders.

## Usage
1. Launch the game.
2. Open Tesla Menu / EdiZon and enable **"D-Pad Down solves Tetromino"**.
3. Enter a Sigil puzzle and press **D-Pad Down**.

## Important: no developer-cheats negative side effects

This cheat uses the **same built-in instant-solve function** that is
normally exposed through the game's developer cheats, but it does
**not enable the developer cheat system itself**.

This distinction is important: when the official developer cheats
are enabled, the game marks the save as having **cheats used**.
It also permanently displays the **"Cheats Available"** notification
in the game.

This Atmosphere cheat does **not** enable developer cheats and does
not set the game's cheat-used flag, but only calls the underlying
Sigil Arranger instant-solve function directly.

---

## How it was created

**The Talos Principle contains developer/debug functionality that can instantly solve a Sigil Arranger puzzle.**

This functionality is exposed in the PC version through the game's developer cheat system. When developer cheats are enabled, right-clicking the **Reset** button in the Sigil Arranger interface triggers a special debug function that instantly solves the puzzle.

The goal was therefore not to create another puzzle solver, but to locate the existing game function inside the Switch executable and make it accessible through an Atmosphere cheat.

The Switch executable was then analysed to locate the corresponding Sigil Arranger/debug code. After identifying the relevant internal code path, the corresponding instruction was tested through an Atmosphere cheat.

The final cheat redirects the action to that existing game functionality when **D-Pad Down** is pressed.

In other words, this is essentially a **one-button interface to a developer function that was already inside the game**.

</details>

<details>
<summary><b>Русский</b></summary>

Чит-код для Atmosphere (Nintendo Switch), который решает паззлы с сигилами (тетрамино) в *The Talos Principle* нажатием кнопки D-Pad Down (вниз на крестовине).

## Описание
- Для решения паззла активируется  встроенная отладочная функция игры.
- Не решает каждый паззл сразу автоматически, а только по нажатию кнопки D-Pad Down.
- **Необходимо сначала собрать нужные для паззла сигилы.** Чит только автоматизирует процесс решения, но не создает недостающие сигилы.

## Требования
- Nintendo Switch с прошивкой Atmosphere
- Игра *The Talos Principle* версии **v1.0.2** (Title ID: `010092A00D43C000`, Build ID: `74562DD37142F8EB`)
- EdiZon или Tesla Menu

## Установка
1. Скачай репозиторий (зелёная кнопка "Code" → "Download ZIP") и распакуй его.
2. Скопируй папку `atmosphere` в корень SD-карты.
3. При запросе операционной системы подтверди слияние папок.

## Использование
1. Запусти игру.
2. Открой Tesla Menu / EdiZon и включи чит **"D-Pad Down solves Tetromino"**.
3. Зайди в паззл с сигилами и нажми **D-Pad Down** (вниз на крестовине).

## Важно: нет негативных побочных эффектов от включения "читов разработчика"

Этот чит использует **ту же встроенную функцию мгновенного решения**,
которая обычно доступна через developer cheats игры, но при этом
**не включает саму систему developer cheats**.

Это важное различие, т.к. при обычном включении developer cheats игра
помечает сохранение как **использовавшее читы**. После загрузки такого
сохранения, постоянно отображается неотключаемая надпись **«Доступны читы»**.

А данный чит просто напрямую вызывает встроенную функцию для мгновенного
решения паззла, **не включая developer cheats**, поэтому **не имеет
описанных выше негативных побочных эффектов**.

---

## Как это было сделано

В **The Talos Principle** разработчики оставили внутри игры отладочную функциональность, позволяющую **мгновенно решить Sigil Arranger**.

В PC-версии эта функциональность доступна через developer cheats. При включённых developer cheats нажатие на кнопку сброса правой кнопкой мыши вызывает мгновенную автосборку паззла.

Поэтому искать отдельный алгоритм решения тетрамино на Switch не требовалось.

Задача состояла в том, чтобы найти соответствующую внутреннюю debug-функцию в исполняемом файле Switch-версии.

После анализа кода Sigil Arranger и связанной с ним debug-логики была найдена соответствующая внутренняя функция. Затем её вызов был проверен непосредственно на Switch и использован для создания Atmosphere cheat-кода.

В результате при нажатии **D-Pad Down** чит не решает тетрамино самостоятельно, а инициирует выполнение уже существующей в игре функции.

</details>
