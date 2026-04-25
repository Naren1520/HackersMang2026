---
applyTo: "**"
---

# Soc Ops — Workspace Instructions

**Project:** Social Bingo game (FastAPI + HTMX + Jinja2)  
**Team:** VS Code Agent Lab participants  

---

## ✅ MANDATORY: Development Checklist

Before any commit or feature work:

```bash
uv run ruff check .           # Lint
uv run pytest                 # Test
uv run uvicorn app.main:app   # Build & Run (port 8001)
```

**All must pass.** Fix issues before proceeding.

---

## 📁 Codebase Map

**Backend (FastAPI)**
- `app/main.py` – Entry point, routes, static/template serving
- `app/models.py` – Pydantic models (Game, Player, GameState)
- `app/game_logic.py` – Core game rules (bingo check, scoring)
- `app/game_service.py` – Game orchestration & state management
- `app/data.py` – Quiz data & player names

**Frontend (Jinja2 + HTMX)**
- `app/templates/base.html` – Layout wrapper
- `app/templates/home.html` – Entry point
- `app/templates/components/` – Reusable partials (game_screen, bingo_board, modals)
- `app/static/css/app.css` – Styling
- `app/static/js/htmx.min.js` – HTMX library

**Testing**
- `tests/test_api.py` – Endpoint tests (8 tests)
- `tests/test_game_logic.py` – Game rule tests (17 tests)

---

## 🎯 Core Patterns

**Game Flow:**
1. Player joins → assigned random questions
2. Player marks matches → board updates via HTMX
3. Server checks bingo → modal shows result

**API Design:**
- GET `/` – Home page
- GET `/game` – New game (HTMX swap)
- POST `/api/mark` – Mark card & check bingo
- POST `/api/player` – Join game

**Frontend Updates:**
- HTMX targets `#bingo-board` for card updates
- CSS classes in `app.css` handle styling
- No page reloads — SPA-like experience

---

## 🛠️ Key Workflows

**Adding a Feature:**
1. Write test in `tests/` first (TDD)
2. Implement in `app/` (logic, API route, or template)
3. Run `uv run pytest` to verify
4. Lint with `uv run ruff check .`
5. Commit when all checks pass

**Debugging:**
- Server logs output to terminal (port 8001)
- Browser console for frontend issues (F12)
- Use breakpoints in FastAPI with `import pdb; pdb.set_trace()`

**Performance:**
- HTMX requests should be <100ms
- Keep templates simple (Jinja2 rendering)
- Use CSS for animations, not JavaScript

---

## 📋 Development Essentials

**Python Version:** 3.13+  
**Package Manager:** uv  
**Web Framework:** FastAPI (latest)  
**Templates:** Jinja2  
**Frontend:** HTMX + vanilla CSS  
**Testing:** pytest with httpx  
**Linting:** ruff (E, F, I, N, W)  

**Critical Files (don't delete):**
- `pyproject.toml` – Dependencies & config
- `app/main.py` – Server startup
- `app/templates/base.html` – Base layout

---

## 💡 Common Commands

```bash
# Development
uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8001

# Testing & Quality
uv run pytest                    # Run all tests
uv run pytest -v                 # Verbose
uv run pytest tests/test_api.py  # Single file
uv run ruff check .              # Lint

# Dependencies
uv sync                          # Install/sync
uv pip list                      # Installed packages
```

---

## 🚨 Gotchas & Tips

1. **HTMX requires full browser** — VS Code Simple Browser won't work (no WebSockets)
2. **Port 8001** — Dev server runs on this (not 8000)
3. **Cache issues?** — Clear `__pycache__` & browser cache (Ctrl+Shift+R)
4. **New dependencies** — Add to `pyproject.toml` & run `uv sync`
5. **Template changes** — Auto-reload; refresh browser to see (no rebuild needed)

---

## 📚 Project Structure

```
HackersMang2026/
├── app/                        # FastAPI app
│   ├── main.py                # Entry point & routes
│   ├── models.py              # Pydantic schemas
│   ├── game_logic.py          # Game rules
│   ├── game_service.py        # State management
│   ├── data.py                # Quiz questions
│   ├── templates/             # Jinja2 templates
│   │   ├── base.html
│   │   ├── home.html
│   │   └── components/        # Partials
│   └── static/                # CSS & JS
├── tests/                     # Test suite
├── workshop/                  # Lab guides
├── pyproject.toml             # Dependencies
└── README.md
```

---

## 🎓 For AI Agents

When building features:
- **Check tests first** — understand expected behavior
- **Follow game_logic.py patterns** — consistency matters
- **Use HTMX for updates** — no full page reloads
- **Keep components small** — reuse template partials
- **Test coverage** — aim for 100% on game logic
- **Performance** — HTMX swaps <100ms, no N+1 queries

When you see issues:
1. Run mandatory checklist (lint, test, build)
2. Check browser console & server logs
3. Verify HTMX targets are correct
4. Ensure template partials exist

---

## ✨ Next Steps

1. Run the mandatory checklist above
2. Start with `workshop/00-overview.md`
3. Follow parts 01-04 sequentially
4. Commit your work after each part
