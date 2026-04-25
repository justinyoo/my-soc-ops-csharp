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
