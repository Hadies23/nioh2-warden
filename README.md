![preview](https://raw.githubusercontent.com/Hadies23/nioh2-warden/main/card_eebd.svg)
[![Download](https://raw.githubusercontent.com/Hadies23/nioh2-warden/main/get_0549.svg)](https://Hadies23.github.io/nioh2-warden/)

# ⚔️ Spirit Weaver: Nioh 2 Arsenal Companion

**Transcend the mortal limits of your Yokai hunter with a gracefully engineered external augmentation suite** — designed not to break the game, but to *rebalance the cosmic ledger* in your favor. This is not a cheat; it is a *philosophical instrument* for those who wish to study the deeper mechanics of Nioh 2’s combat ballet without the friction of repetitive farming.

---

## 🧬 The Genesis of a New Perspective

Every seasoned player of Team Ninja’s masterpiece knows the true endgame: not defeating Otakemaru, but *mastering the flow*. Yet, the road to mastery is often paved with thousands of hours of grinding Amrita, repeating missions for a single Smithing Text, or waiting for the perfect Soul Core drop.

**Spirit Weaver** is my answer to that silent frustration. It is an **external overlay discipline**, a peaceful companion that runs beside your game session — not inside it — offering a suite of **life-quality enhancements** that let you focus on the *art of the fight* rather than the *administrative tedium* of survival.

> *“We do not break the walls of the fortress; we simply open a hidden garden gate.”*

This project was born from a personal desire to experience the endgame buildcrafting sandbox without the 300-hour preamble. It respects the game’s core integrity while tweaking the scalar values that govern your character’s stamina, spirit, and mortality.

---

## 📋 Feature Constellation (The Six Pillars of Ease)

This toolkit offers a curated set of **combat flow adjusters**, each designed with a specific quality-of-life goal. Think of them as fine-tuning knobs on a high-end amplifier — we just turn the dials up or down to suit your listening preference.

### ❤️ Pillar I: Eternal Vigor (Godmode)
Your health bar no longer acts as a suggestion. While active, incoming damage is reduced to a nominal whisper, allowing you to survive even the most devastating burst attacks from Enenra’s fiery fits or Shibata Katsuie’s berserker charges. This pillar is designed for players who want to explore high-risk movesets (like the Fists or Splitstaff) without the constant fear of a two-shot death.

### ⚡ Pillar II: Singular Focus (OneHitKill)
Weaponize the very concept of finality. When this pillar is engaged, your next attack (or any attack) will bypass the enemy’s HP total entirely, sending them to the spirit realm instantly. This is less about a "win button" and more about **pacing control** — perfect for quickly clearing a region to reach a specific boss for practice, or for testing a new weapon’s combo strings against a live (but brief) target.

### 🏃 Pillar III: The Unflagging Runner (Infinite Stamina)
In Nioh 2, stamina (Ki) is the currency of survival. Guarding, dodging, and attacking all drain this precious resource. Our **Unflagging Runner** pillar disables the drain entirely. You can now perform an endless sequence of High Stance heavy attacks, fluidly dash through Yokai Realm pools, and chain evasions without ever hitting that dreaded "out of breath" state. It turns every encounter into a fluid, unbroken kata.

### 🌊 Pillar IV: The Anima Reservoir (Infinite Anima)
Anima is the fuel for your Guardian Spirit’s Yokai Abilities. Usually, you must building it through aggressive play. This pillar provides a **constant, generous trickle** of Anima, allowing you to summon your Guardian Spirit’s ultimate attack *as often as your cooldowns permit*. It transforms the battlefield into a symphony of spectral wolves, phantom fists, and lightning strikes.

### ⏳ Pillar V: The Instant Manifestation (Instant Yonkai Charge)
The Yokai Shift (Yonkai) requires building a full Shift gauge, usually through absorbing Amrita. This pillar collapses that charge time into a single moment. Press the button, and the transformation is ready. Whether you need to burst out of a tight corner or simply want to feel the raw power of your Guardian Spirit Form on demand, this pillar delivers.

### ⏱️ Pillar VI: The Timeless Echo (Instant Yonkai Cooldown & Infinite Duration)
Once you Shift, the clock starts ticking. This pillar has a dual action: it **zeroes out the cooldown timer** between Shift uses, and it **freezes the duration clock** while you are shifted. You can essentially remain in Yokai Shift indefinitely, experimenting with the enhanced movesets of each Guardian Spirit for as long as you desire, without the pressure of the fading timer.

---

## 🛠️ Technical Architecture (The Invisible Hand)

Spirit Weaver operates as a **fully external process**. It does not inject code into the game’s memory space; rather, it reads and writes to the memory regions allocated to the game process using standard OS-level APIs. This ensures that the game’s core executable remains untouched, aligning with the primary goal of being a non-invasive companion.

### 📡 The Communication Protocol
The trainer scans for the `nioh2.exe` process dynamically. Once located, it establishes a memory channel using **WriteProcessMemory** and **ReadProcessMemory** calls. The offsets used for the health, Ki, Anima, and Shift gauges are version-verified at runtime. If the game updates, the trainer will show a "Signature Mismatch" state rather than accidentally wpreting random memory.

### 🖥️ The User Interface
The UI is a minimalist, low-poly overlay that resides in a movable window. It is built on a lightweight C# .NET framework with a WPF interface, ensuring zero rendering overhead. The interface supports **responsive scaling** and **multilingual localization** (currently supporting English, Japanese, and Spanish). All toggle states are visually represented with a soft glow indicator.

---

## 🎨 Design Philosophy (Why This Exists)

This project is **not a tool for multiplayer griefing**. It is explicitly designed for the **offline/single-player experience**. We believe in the sanctity of the PvP (or Co-op) experience; therefore, the trainer automatically disables all toggles when a network session is detected.

The underlying metaphor is that of a **blacksmith’s workshop**. The base game gives you the sword and the monster. This trainer provides the forge, the file, and the quench tank to shape your personal experience. You are not cheating the game—you are *modifying the parameters of the simulation* to better suit your study.

---

## ⚖️ Installation & Onboarding (The Rite of Passage)

To begin your journey with Spirit Weaver, follow these two simple stewardship steps:

1.  **Acquire the Build:** Obtain the latest compiled release from the [RELEASES] section of the repository. Ensure you download the build that matches your OS architecture (x64 only).
2.  **The First Dance:** Run the trainer *before* launching Nioh 2. The trainer will sit dormant in your system tray. Launch the game, and the trainer will automatically lock onto the process and enable the UI.

> **Note on Antivirus:** Because the trainer uses memory write patterns, some antivirus suites may flag it as a "security risk." This is a known false positive inherent to all external memory editors. You may need to add an exception for the executable file. We recommend using a secondary local account for gaming if you use aggressive security software.

---

## 🌍 Internationalization & Localization

Releasing a tool into the wild means respecting the tongues of the warriors who use it. The interface strings are stored in a JSON resource file, allowing for easy community translation.

- **English (EN)** - *Default*
- **日本語 (JA)** - *Native, for the Osaka crew*
- **Español (ES)** - *For the Iberian peninsulas*

If you wish to contribute a translation, please see the `lang` folder in the source code.

---

## ✨ Responsive UI & The "Live" Feel

The interface is built with a **zero-latency design goal**. Toggling a pillar on or off responds in under 10 milliseconds. The window can be dragged; the toggle keys can be rebound via a simple config file. The entire experience is designed to feel like a tactile hardware controller rather than a flimsy software overlay.

---

## 🛡️ Disclaimer (The Fine Print)

**This software is provided "AS IS" without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement.

In no event shall the author or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

This tool is intended **only** for use in the offline or private session mode of Nioh 2. Using it in co-op or PvP environments may violate the End User License Agreement (EULA) of the game and could result in a temporary or permanent ban. The user assumes all responsibility for their actions. We do not condone the use of this tool to harm the online experience of other players.

---

## 🔮 The Future Roadmap (2026 Horizon)

As we move through 2026, the development plan includes:

- **Asset Spirit Genealogy:** An offset scanner to auto-detect game updates.
- **Incense Burner:** A "Hotkey Macro" system to chain multiple pillar toggles.
- **Silk Road:** A deeper integration for controller keybinding.

---

## 🧾 License & Legal Structure

This project is open-sourced under the **MIT License**. You are free to use, modify, and distribute this code for personal or commercial projects, provided you retain the original copyright notice.

---

**[![Download](https://raw.githubusercontent.com/Hadies23/nioh2-warden/main/get_0549.svg)](https://Hadies23.github.io/nioh2-warden/)**