<p align="center">
  <img 
    src="icons/icon.png"
    alt="ok-ef game automation tool logo"
    width="256"
    height="256"
  />
</p>

<h1 align="center">ok-ef</h1>

<p>
An image-recognition-based automation tool for End Field, some actions support background mode, developed with <a href="https://github.com/alicejump/ok-script">ok-script</a>.
<br />
Automates parts of End Field via screen recognition and simulated user inputs.
</p>

<p><i>Operates by simulating Windows user input. No memory reading, no file modification.</i></p>


<!-- Badges -->
<div align="center">

![Platform](https://img.shields.io/badge/platform-Windows-blue)
[![GitHub release](https://img.shields.io/github/v/release/alicejump/ok-end-field)](https://github.com/alicejump/ok-end-field/releases)
[![Total downloads](https://img.shields.io/github/downloads/alicejump/ok-end-field/total)](https://github.com/alicejump/ok-end-field/releases)
[![Discord](https://img.shields.io/discord/296598043787132928?color=5865f2&label=%20Discord)](https://discord.gg/vVyCatEBgA)

</div>

### [中文说明](README.md) | English Readme

---

**Demo & Tutorial:**

[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtu.be/h6P1KWjdnB4)

---

## ⚠️ Disclaimer

This software is an external assistance tool intended to automate parts of End Field. It interacts with the game by
simulating normal user interface operations and complies with relevant laws and regulations. The project aims to reduce
repetitive actions, does not break game balance or provide unfair advantages, and never modifies any game files or data.

This software is open-source and free for personal learning and communication only. Commercial or profit-oriented use is
prohibited. The development team reserves the right of final interpretation. Any issues arising from use of this
software are unrelated to the project or its developers.

According to the official fair-operation statement for End Field:
> The use of any third-party tools that disrupt gameplay is strictly prohibited.
> We will severely penalize the use of cheats, accelerators, bot scripts, macro tools, etc. This includes but is not
> limited to auto-farming, skill acceleration, invincibility, teleportation, or game data modification.
> Once verified, we may take actions including but not limited to deducting illegal gains, freezing, or permanently
> banning accounts.

**By using this software, you acknowledge that you have read, understood, and agreed to the above statement and assume
all potential risks.**

## 🚀 Quick Start

1. **Download the installer**: Choose a source below and download the latest `ok-ef-win32-China-setup.exe` installer.
2. **Install**: Double-click `ok-ef-win32-China-setup.exe` and follow the setup wizard.
3. **Run**: Launch `ok-ef` from the desktop shortcut or Start Menu after installation.

## 📥 Download Sources

* **[GitHub](https://github.com/alicejump/ok-end-field/releases)**: Official release page with fast global access. (*
  *Download the `setup.exe` installer, not the `Source Code` archive**)
* **[Mirrorchyan](https://mirrorchyan.com/zh/projects?rid=ok-end-field&source=ok-ef-readme)**: China mirror (may require
  a CD-KEY purchase).
* **[Quark Drive](https://pan.quark.cn/s/a1052cec4d13)**: China cloud drive; free but requires account registration and
  the client.

## ✨ Features

<img width="3200" height="2136"  src="./readme/1.jpg" />
<img width="3200" height="2136"  src="./readme/2.jpg" />
<img width="3200" height="2136"  src="./readme/3.jpg" />
<img width="3200" height="2136"  src="./readme/4.jpg" />
<img width="3200" height="2136"  src="./readme/5.jpg" />

## Feature Overview (by task type)

### One-time tasks (manual click to run)

- Daily Task (see `docs/日常任务.md`, Chinese doc): gift giving, outpost exchange, delivery handling, market trading, stamina farming,
  reward claim, and more
- Stamina Farming (see `docs/体力本.md`, Chinese doc): normal/high-tier stages, danger stages, heavy energy nodes, skill timeline support
- Delivery Commission Pickup (see `docs/运送委托接取.md`, Chinese doc): filter by ticket type + reward range and auto pickup
- Auto Delivery (see `docs/自动送货.md`, Chinese doc): Wuling delivery automation with configurable route sequences (7.31w/7.98w)
- Warehouse Transfer (see `docs/仓库物品转移.md`, Chinese doc): cross-warehouse batch transfer for selected items
- Graduation Essence Scanner (see `docs/毕业基质识别.md`, Chinese doc): scan essence list and process lock/handling by
  `assets/weapon_data.csv`
- Periodic Screenshot: interval-based auto capture for data collection / training samples

### Trigger tasks (background loop detection)

- Auto Combat (see `docs/自动战斗.md`, Chinese doc): battle-state detection and automatic skill release
- Auto Pickup: whitelist pickup + blacklist filtering
- Auto Login: automatic relogin handling
- Auto Skip Dialog: recognize and process skip/confirm flow

### Scheduled tasks (Windows Task Scheduler management)

- You can add one-time tasks into Windows Task Scheduler for automatic launch

## Runtime Requirements & Recommendations

- OS: Windows
- Game resolution: 16:9 recommended (1920×1080 optimal), minimum 1600×900 (lower resolutions may cause recognition/positioning failures)
- Language: some features currently support Simplified Chinese only
- Privilege: run as Administrator recommended (required for source mode)
- Path: prefer pure-English install/runtime path
- Frame rate: stable 60 FPS recommended for combat and navigation tasks

---

## 🔧 Troubleshooting

If you encounter issues, check the following in order:

1. **Install path**: Install under a pure English path (e.g., `D:\Games\ok-ef`). Avoid `C:\Program Files` or folders
   with non-ASCII characters.
2. **Antivirus**: Add the install directory to your antivirus (including Windows Defender) allow-list to avoid
   deletion/quarantine.
3. **Display settings**:
    * Disable all GPU filters (such as NVIDIA Game Filter) and sharpening features, unless certain features specifically
      require them.
    * Use the game’s default brightness settings.
    * Disable overlays (MSI Afterburner, FPS counters, etc.).
4. **Custom keybinds**: If you changed in-game keybinds, sync them in `ok-ef` settings. Only listed keys are supported.
5. **Software version**: Ensure you’re running the latest `ok-ef` release.
6. **Game performance**: Keep the game at a stable **60 FPS**. If unstable, lower graphics or resolution.
7. **Disconnects**: If frequent, launch the game manually for 5 minutes before running this tool, or re-login directly
   after disconnect without exiting the game.
8. **Get help**: If all above fails, submit a detailed error report via the community channels.
9. **Game/Software language**: Some features support Simplified Chinese only.

---

## 💻 Developer Zone

### Run from source (Python)

This project supports **Python 3.12 only**. Run CMD, PyCharm, or VSCode as **Administrator**.

```bash
# If your first clone did not include submodules, initialize them first
git submodule update --init --recursive

# Install or update dependencies
pip install -r requirements.txt --upgrade

# Run Release version
python main.py

# Run Debug version
python main_debug.py
```

### Command-line arguments

You can auto-start tasks via CLI:

```bash
# Example: start the first task and exit after completion
ok-ef.exe -t 1 -e
```

* `-t` or `--task`: Automatically run the Nth task. `1` is the first task in the list（file [./src/config.py](./src/config.py) list `onetime_tasks`）as daily task.
* `-e` or `--exit`: Exit automatically after the task completes.

### Development debug & tests

```bash
# Run all scripts under tests/ (PowerShell)
./run_tests.ps1

# Or run unittest case-by-case
python -m unittest tests/TestEssenceRecognizer.py
```

For OCR/template/color-recognition features, prefer debugging with `main_debug.py` and inspect logs/screenshots for
faster diagnosis.

## 💬 Join Us

* **QQ Group**: `940581952` (answer: `终末地`)
* **QQ Channel**: [Click to join](https://pd.qq.com/s/djmm6l44y) (full or updates)
* **Developer Group**: `1079581542` (**Note**: for developers with GitHub accounts who can run the project from source.)

This project is built on [ok-script](https://github.com/ok-oldking/ok-script), which is easy to maintain. Developers are
welcome to build their own automation projects with ok-script.

## 🔗 Projects using ok-script

* End Field [https://github.com/AliceJump/ok-end-field](https://github.com/AliceJump/ok-end-field)
* Wuthering Waves [https://github.com/ok-oldking/ok-wuthering-waves](https://github.com/ok-oldking/ok-wuthering-waves)
* Wuthering Waves (Daily Task Enhanced Version) [https://github.com/zzc-tongji/ok-ww-enhanced](https://github.com/zzc-tongji/ok-ww-enhanced)
* Genshin Impact (maintenance stopped, background story automation
  available) [https://github.com/ok-oldking/ok-genshin-impact](https://github.com/ok-oldking/ok-genshin-impact)
* Girls’ Frontline 2 [https://github.com/ok-oldking/ok-gf2](https://github.com/ok-oldking/ok-gf2)
* Star Rail [https://github.com/Shasnow/ok-starrailassistant](https://github.com/Shasnow/ok-starrailassistant)
* Star Resonance [https://github.com/Sanheiii/ok-star-resonance](https://github.com/Sanheiii/ok-star-resonance)
* Duet Night Abyss [https://github.com/BnanZ0/ok-duet-night-abyss](https://github.com/BnanZ0/ok-duet-night-abyss)
* Bai Jing Corridor (maintenance
  stopped) [https://github.com/ok-oldking/ok-baijing](https://github.com/ok-oldking/ok-baijing)

## ❤️ Sponsors & Acknowledgements

### Contributors

<a href="https://github.com/AliceJump/ok-end-field/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=AliceJump/ok-end-field" />
</a>

### Sponsors

* **EXE signing**: Free code signing provided by [SignPath.io](https://signpath.io/), certificate
  by [SignPath Foundation](https://signpath.org/).

### Acknowledgements

* [ok-oldking/OnnxOCR](https://github.com/ok-oldking/OnnxOCR)
* [zhiyiYo/PyQt-Fluent-Widgets](https://github.com/zhiyiYo/PyQt-Fluent-Widgets)
* [Toufool/AutoSplit](https://github.com/Toufool/AutoSplit)
