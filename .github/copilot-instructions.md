# Copilot Workspace Instructions

## Before Every Commit

- [ ] `dotnet build SocOps/SocOps.csproj` — 0 errors, 0 warnings
- [ ] `dotnet test` — all tests pass (no-op until a test project exists)
- [ ] No unused variables, imports, or dead code

## Project

**SocOps** — SOC-themed Social Bingo, Blazor WebAssembly (.NET 10). Players mark squares by finding people matching questions; first 5-in-a-row wins.

```bash
dotnet run --project SocOps/SocOps.csproj  # → http://localhost:5166
```

## Architecture

| Folder | Responsibility |
|---|---|
| `Components/` | `BingoBoard`, `BingoSquare`, `BingoModal`, `GameScreen`, `StartScreen` |
| `Services/` | `BingoGameService` — state + localStorage · `BingoLogicService` — pure logic, no DI |
| `Data/Questions.cs` | Question bank — add new questions here |
| `wwwroot/css/app.css` | Custom Tailwind-like utilities — source of truth for styling |

## Conventions

- **State**: `BingoGameService` owns all mutable state; components subscribe to `OnStateChanged`, never mutate directly.
- **Logic**: `BingoLogicService` is stateless/pure — keep it that way.
- **CSS**: Prefer existing utilities in `app.css`. See `.github/instructions/css-utilities.instructions.md`.
- **C#**: PascalCase public members · nullable enabled · implicit usings on.
- **Reference implementations**: `.solutions/step-01-*` → `.solutions/finished/`

## Design Guide

The app uses a **Minecraft-inspired** visual theme. All UI decisions must stay consistent with this aesthetic.

### Theme Language

| Element | Treatment |
|---|---|
| Typography — headings | `PressStart2P` pixel font via `.mc-title` |
| Typography — body/labels | `VT323` monospace via default `body` font |
| Backgrounds | Stone/grass/sky layered gradients — no flat solid colours |
| Borders | Hard pixel edges (`border-radius: 0`) with stacked `box-shadow` for depth |
| Shadows | Offset hard shadows (e.g. `0 4px 0 #2a1b12`) — no blurred drop shadows |
| Animations | CSS `steps()` timing — no `ease` or `cubic-bezier` easing for theme motion |
| Transitions | 80 ms stepped (`steps(2, end)`) — snappy, not smooth |

### CSS Architecture

- All theme classes are prefixed `mc-` and live in `wwwroot/css/app.css`.
- Fonts are bundled at `wwwroot/fonts/` (PressStart2P-Regular.ttf, VT323-Regular.ttf) — **do not load from a CDN**.
- Legacy Tailwind-like utilities (`.flex`, `.grid-cols-5`, etc.) are preserved for layout only; do not use them for colour or border styling — use `mc-*` classes instead.
- CSS custom properties are defined in `:root` under the `--mc-*` namespace.

### Key `mc-*` Classes

| Class | Purpose |
|---|---|
| `.mc-screen` | Full-height page wrapper with atmospheric gradient background |
| `.mc-header` | Top navigation bar (dirt-brown gradient, pixel bottom border) |
| `.mc-panel` | Content card with dirt/wood gradient and hard shadow |
| `.mc-board-frame` | Stone-textured container wrapping the 5×5 bingo grid |
| `.mc-square` | Base bingo cell (wood block, uppercase text, pixel shadow) |
| `.mc-square-marked` | Marked cell (emerald green block) |
| `.mc-square-winning` | Winning cell (diamond blue block, pulsing animation) |
| `.mc-square-free` | Free-space centre cell (gold block, PressStart2P font) |
| `.mc-btn` | Primary action button (grass green gradient, press effect) |
| `.mc-btn-secondary` | Secondary/navigation button (stone gradient) |
| `.mc-modal` | Victory modal card |
| `.mc-modal-backdrop` | Full-screen overlay with radial glow effects |
| `.mc-banner` | In-game bingo notification strip (diamond-blue, animated) |
| `.mc-title` | PressStart2P heading with green drop shadow |
| `.mc-subtitle` | Small-caps PressStart2P subtitle |
| `.mc-note` | Instructional note panel (dark wood background) |
| `.mc-check` | Marked-square indicator badge (PressStart2P, top-right) |
| `.mc-reveal` | Entry animation (fade + slide, `steps(3, end)`) |
| `.mc-start-float` | Idle float loop for hero elements |

### Adding New Screens or Components

1. Wrap page-level content in `.mc-screen`.
2. Use `.mc-panel` for any card/box that groups content.
3. Use `.mc-btn` (primary) or `.mc-btn-secondary` (navigation/cancel) for all interactive buttons.
4. Always inherit `VT323` body font for regular text; apply `.mc-title` only for headings.
5. Do not introduce new `border-radius`, `box-shadow blur`, or `transition ease` values — they break the pixel aesthetic.
6. Add any new `mc-*` utility classes to `app.css` following the existing naming pattern.
7. Provide a `@media (prefers-reduced-motion: reduce)` exemption for any new keyframe animations.
