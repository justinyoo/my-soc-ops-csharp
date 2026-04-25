🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

<div align="center">

# 🎯 SocOps

### Social Bingo for in-person mixers — built with Blazor & GitHub Copilot

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?style=flat-square&logo=dotnet)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WASM](https://img.shields.io/badge/Blazor-WebAssembly-592BD4?style=flat-square&logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-222222?style=flat-square&logo=github)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

**[🎮 Play Now](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)** &nbsp;|&nbsp; **[📚 Lab Guide](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/)**

</div>

---

## What is SocOps?

**SocOps** is a real-time Social Bingo game for conferences, meetups, and team events. Players mingle, ask each other the questions on their card, and race to get **5 in a row** — first to BINGO wins! 🏆

This repo is also the starting point for a hands-on **VS Code + GitHub Copilot Agent Lab**, where you'll transform this app step by step using AI-assisted development.

---

## 🎮 How to Play

1. **Start a new game** — a unique 5×5 bingo card is generated just for you
2. **Mingle!** — find someone in the room who matches each square (e.g., _"bikes to work"_, _"plays an instrument"_)
3. **Mark the square** — tap or click to mark it when you find a match
4. **BINGO!** — get 5 in a row (across, down, or diagonally) and celebrate 🎉

---

## 🧪 VS Code Copilot Agent Lab

This project is the hands-on playground for the **VS Code GitHub Copilot Agent Lab** — a ~1 hour workshop covering:

| # | Part | Skill | Time |
|---|------|-------|------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Overview & Checklist | Lab orientation | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Setup & Context Engineering | Teach AI your codebase | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Design-First Frontend | AI-guided UI redesign | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Custom Quiz Master | Build a custom agent | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Multi-Agent Development | TDD + design agents | 20 min |

> 📝 Lab guides are also available [online](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/) and in the [`workshop/`](workshop/) folder for offline reading.

---

## 🚀 Getting Started

### Prerequisites

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) or higher
- [VS Code](https://code.visualstudio.com/) with [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

### Run locally

```bash
cd SocOps
dotnet run
```

Then open [http://localhost:5166](http://localhost:5166) in your browser.

### ☁️ Open in GitHub Codespaces

The fastest way to get started — no local setup required:

1. Click **Use this template** → **Create a new repository**
2. Open your repo → **Code** → **Codespaces** → **Create codespace on main**
3. Wait for the devcontainer to finish setup
4. Run `cd SocOps && dotnet run` in the terminal

### Build

```bash
cd SocOps
dotnet build
```

Deploys automatically to GitHub Pages on push to `main`.

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Blazor WebAssembly (.NET 10) |
| Styling | Custom CSS utilities (Tailwind-like) |
| State | In-memory service + `localStorage` |
| Deploy | GitHub Pages (auto on push to `main`) |

---

## 📁 Project Structure

```
SocOps/
├── Components/      # BingoBoard, BingoSquare, BingoModal, GameScreen, StartScreen
├── Data/            # Questions.cs — question bank
├── Services/        # BingoGameService (state), BingoLogicService (pure logic)
└── wwwroot/css/     # app.css — styling source of truth
```

---

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

<div align="center">

Built with ❤️ for in-person developer events

</div>
