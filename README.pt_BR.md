<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎯 SocOps

### Social Bingo para encontros presenciais — construído com Blazor e GitHub Copilot

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?style=flat-square&logo=dotnet)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WASM](https://img.shields.io/badge/Blazor-WebAssembly-592BD4?style=flat-square&logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-222222?style=flat-square&logo=github)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

**[🎮 Jogar](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)** &nbsp;|&nbsp; **[📚 Guia do Lab](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/)**

</div>

---

## O que é SocOps?

**SocOps** é um jogo de Social Bingo em tempo real para conferências, meetups e eventos de equipe. Os jogadores circulam, fazem perguntas uns aos outros e competem para conseguir **5 em fila** — quem gritar BINGO primeiro, ganha! 🏆

Este repositório também é o ponto de partida para um **VS Code + GitHub Copilot Agent Lab** prático, onde você vai transformar este app passo a passo usando desenvolvimento assistido por IA.

---

## 🎮 Como Jogar

1. **Inicie um novo jogo** — um cartão único 5×5 é gerado só para você
2. **Circule!** — encontre alguém na sala que corresponda a cada quadrado (ex.: _"vai ao trabalho de bicicleta"_, _"toca um instrumento"_)
3. **Marque o quadrado** — toque ou clique para marcar quando encontrar uma correspondência
4. **BINGO!** — consiga 5 em fila (horizontal, vertical ou diagonal) e comemore! 🎉

---

## 🧪 VS Code Copilot Agent Lab

Este projeto é o playground prático para o **VS Code GitHub Copilot Agent Lab** — um workshop de ~1 hora cobrindo:

| # | Parte | Habilidade | Tempo |
|---|-------|------------|-------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Visão Geral & Lista Rápida | Orientação do lab | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Configuração & Engenharia de Contexto | Ensine IA sobre seu código | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Frontend Design-First | Redesign de UI com IA | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | Crie um agente próprio | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Desenvolvimento Multi-Agent | TDD + agentes de design | 20 min |

> 📝 Os guias do lab também estão disponíveis na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## 🚀 Primeiros Passos

### Pré-requisitos

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) ou superior
- [VS Code](https://code.visualstudio.com/) com [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

### Executar localmente

```bash
cd SocOps
dotnet run
```

Abra [http://localhost:5166](http://localhost:5166) no seu navegador.

### ☁️ Abrir no GitHub Codespaces

A forma mais rápida de começar — sem configuração local:

1. Clique em **Use this template** → **Create a new repository**
2. Abra seu repositório → **Code** → **Codespaces** → **Create codespace on main**
3. Aguarde a configuração do devcontainer finalizar
4. Execute `cd SocOps && dotnet run` no terminal

### Compilar

```bash
cd SocOps
dotnet build
```

O deploy é feito automaticamente no GitHub Pages ao fazer push para `main`.

---

## 🏗️ Stack Tecnológico

| Camada | Tecnologia |
|--------|------------|
| Frontend | Blazor WebAssembly (.NET 10) |
| Estilos | Utilitários CSS customizados (estilo Tailwind) |
| Estado | Serviço em memória + `localStorage` |
| Deploy | GitHub Pages (automático no push para `main`) |

---

## 📁 Estrutura do Projeto

```
SocOps/
├── Components/      # BingoBoard, BingoSquare, BingoModal, GameScreen, StartScreen
├── Data/            # Questions.cs — banco de perguntas
├── Services/        # BingoGameService (estado), BingoLogicService (lógica pura)
└── wwwroot/css/     # app.css — fonte de verdade dos estilos
```

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Consulte [CONTRIBUTING.md](CONTRIBUTING.md) para mais informações.

---

<div align="center">

Feito com ❤️ para eventos presenciais de desenvolvedores

</div>
