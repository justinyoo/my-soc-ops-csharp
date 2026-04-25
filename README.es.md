<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎯 SocOps

### Social Bingo para encuentros presenciales — construido con Blazor y GitHub Copilot

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?style=flat-square&logo=dotnet)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WASM](https://img.shields.io/badge/Blazor-WebAssembly-592BD4?style=flat-square&logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-222222?style=flat-square&logo=github)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

**[🎮 Jugar](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)** &nbsp;|&nbsp; **[📚 Guía del Lab](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/)**

</div>

---

## ¿Qué es SocOps?

**SocOps** es un juego de Social Bingo en tiempo real para conferencias, meetups y eventos de equipo. Los jugadores se mezclan, se hacen preguntas entre sí y compiten por conseguir **5 en fila** — ¡el primero en gritar BINGO gana! 🏆

Este repositorio también es el punto de partida para un **VS Code + GitHub Copilot Agent Lab** práctico, donde transformarás esta app paso a paso usando desarrollo asistido por IA.

---

## 🎮 Cómo Jugar

1. **Inicia una partida** — se genera un tablero único de 5×5 solo para ti
2. **¡Socializa!** — encuentra a alguien en la sala que coincida con cada casilla (ej., _"va al trabajo en bicicleta"_, _"toca un instrumento"_)
3. **Marca la casilla** — toca o haz clic para marcarla cuando encuentres una coincidencia
4. **¡BINGO!** — consigue 5 en fila (horizontal, vertical o diagonal) y ¡a celebrar! 🎉

---

## 🧪 VS Code Copilot Agent Lab

Este proyecto es el área de trabajo práctica para el **VS Code GitHub Copilot Agent Lab** — un taller de ~1 hora que cubre:

| # | Parte | Habilidad | Tiempo |
|---|-------|-----------|--------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Descripción General & Lista Rápida | Orientación del lab | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Configuración & Ingeniería de Contexto | Enseña IA tu código | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Frontend Design-First | Rediseño de UI con IA | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | Crea un agente propio | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Desarrollo Multi-Agent | TDD + agentes de diseño | 20 min |

> 📝 Las guías del lab también están disponibles en la carpeta [`workshop/es/`](workshop/es/) para lectura offline.

---

## 🚀 Primeros Pasos

### Requisitos Previos

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) o superior
- [VS Code](https://code.visualstudio.com/) con [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

### Ejecutar localmente

```bash
cd SocOps
dotnet run
```

Abre [http://localhost:5166](http://localhost:5166) en tu navegador.

### ☁️ Abrir en GitHub Codespaces

La forma más rápida de empezar — sin configuración local:

1. Haz clic en **Use this template** → **Create a new repository**
2. Abre tu repo → **Code** → **Codespaces** → **Create codespace on main**
3. Espera a que termine la configuración del devcontainer
4. Ejecuta `cd SocOps && dotnet run` en la terminal

### Compilar

```bash
cd SocOps
dotnet build
```

El deploy se hace automáticamente en GitHub Pages al hacer push a `main`.

---

## 🏗️ Stack Tecnológico

| Capa | Tecnología |
|------|------------|
| Frontend | Blazor WebAssembly (.NET 10) |
| Estilos | Utilidades CSS personalizadas (estilo Tailwind) |
| Estado | Servicio en memoria + `localStorage` |
| Deploy | GitHub Pages (automático en push a `main`) |

---

## 📁 Estructura del Proyecto

```
SocOps/
├── Components/      # BingoBoard, BingoSquare, BingoModal, GameScreen, StartScreen
├── Data/            # Questions.cs — banco de preguntas
├── Services/        # BingoGameService (estado), BingoLogicService (lógica pura)
└── wwwroot/css/     # app.css — fuente de verdad de estilos
```

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Consulta [CONTRIBUTING.md](CONTRIBUTING.md) para más información.

---

<div align="center">

Hecho con ❤️ para eventos presenciales de desarrolladores

</div>
