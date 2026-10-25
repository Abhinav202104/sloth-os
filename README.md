<div align="center">

# 🦥 SlothOS: Local Autonomous Dev Agent
### *Slow, Steady & 100% Offline AI for Lazy Developers*

[![Ollama Open Weights](https://img.shields.io/badge/Engine-Ollama%20%7C%20Qwen2.5%20Coder-orange?style=for-the-badge&logo=ollama)](https://ollama.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Air-Gapped Localhost](https://img.shields.io/badge/Privacy-100%25%20Offline%20Localhost-emerald?style=for-the-badge)](http://localhost:4000)
[![Dev Challenge](https://img.shields.io/badge/Theme-Slow%20&%20Steady%20%7C%20Sloth%20Day-purple?style=for-the-badge)](https://dev.to)

</div>

---

## 💡 What is SlothOS?

**SlothOS** is an air-gapped, open-source autonomous developer agent built for International Sloth Day and the **"Slow and Steady"** challenge. It channels maximum developer laziness to automate the two chores every software engineer dreads the most:

1. **🌙 SlothShip (End-of-Day Commit & PR Generator):** Inspects your messy uncommitted working tree across any local repository, runs a local regex privacy sanitizer (`SlothGuard`) to strip out accidental API keys, groups file changes into logical **Atomic Commits**, executes them in one click, and drafts a complete Pull Request description.
2. **☕ SlothStandup (9 AM Standup Synthesizer):** Digests your recent local Git commit history overnight and hands you a 3-column **Yesterday / Today / Blockers** cheat sheet—complete with a built-in browser Web Speech API voice reader that reads your verbatim Zoom script out loud while you make coffee.

---

## 🏗️ System Architecture

```text
[ Local Git Repositories ] 
         │
         ▼ (100% Offline Inspection via Native Git)
[ SlothGuard Privacy Redactor ] ──► Strips API keys / .env secrets locally
         │
         ▼
[ Node.js + Express Agent Harness ]
         ├──► Tool 1: Atomic Diff Analyzer & Auto-Committer
         ├──► Tool 2: PR & Changelog Markdown Drafter
         └──► Tool 3: 9 AM Standup Synthesizer + TTS Voice Reader
         │
         ▼ (Local HTTP API :11434)
[ Ollama Open-Weights Engine: qwen2.5-coder:7b / llama3.2 ]
         │
         ▼
[ React / Tailwind "Sloth Mode" Dashboard ] (One-click Execute & Copy)
```

---

## 🔓 Why Open Innovation Matters Here

You *could* wire scripts like this to a closed commercial cloud API—until you hit real-world engineering constraints:

* **Strict Proprietary Source Code Privacy:** Unstaged `git diff` outputs frequently contain proprietary business logic, internal architecture, or accidentally hardcoded credentials. Piping raw, uncommitted work diffs to a cloud server violates enterprise NDAs. SlothOS runs `qwen2.5-coder` 100% locally on `127.0.0.1` alongside `SlothGuard`, ensuring **not a single byte of source code ever leaves your machine.**
* **Zero Ongoing Cost for Token-Heavy Workflows:** Diffs easily span 5,000–15,000+ tokens. Running an automated agent on every commit using paid APIs burns money fast. With Ollama, SlothOS is **set-it-once, free forever ($\$0.00$ per run)**.
* **True Airplane-Mode Autonomy:** Whether coding on a train or conserving battery, SlothOS works entirely offline with zero latency dependencies.

---

## 🚀 Quickstart Guide

### Prerequisites
* **Node.js** (v18 or higher) installed on your Mac/PC.
* **Ollama** installed locally (`brew install ollama`).

### 1. Clone & Install
```bash
git clone https://github.com/YOUR_USERNAME/sloth-os.git
cd sloth-os
npm install express cors
```

### 2. Pull Your Open-Weight Model
```bash
ollama pull qwen2.5-coder:7b
```
*(Or `ollama pull llama3.2`)*

### 3. Start the SlothOS Backend
```bash
node server.js
```
*Console output:* `🦥 SlothOS Local Agent v3 (Bulletproof Native Git) running on http://localhost:4000`

### 4. Open the Dashboard
Open **`index.html`** in your browser (or run `open index.html` on macOS).

---

## 🧪 How to Test

1. **Leave the Repository Path Box Blank** to test against the `sloth-os` folder itself (or paste the absolute path of any local MERN stack project).
2. Click **🌙 SlothShip (Auto-Commit & PR)** to watch Ollama group your uncommitted changes into atomic commits and generate a PR summary.
3. Click **☕ 9 AM Standup Prep** to review your automated standup cheat sheet and click **🔊 Read Out Loud While I Make Coffee** to hear your browser speak your Zoom script!

---

## 📜 License
Distributed under the **MIT License**. See `LICENSE` for more information.
