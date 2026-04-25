🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# 🎮 Soc Ops — Social Bingo for Mixers

**Find people. Match questions. Get 5 in a row. Win!**

A lightning-fast social bingo game that brings people together at in-person events. Built with modern Python web tech for maximum performance and engagement.

---

## ✨ Why Soc Ops?

| 🎯 | **Purpose** | Play bingo at mixers to meet new people |
| ⚡ | **Speed** | Real-time card updates with HTMX (no page reloads) |
| 🧠 | **Tech** | FastAPI + Jinja2 + HTMX — minimal, powerful, fast |
| 📚 | **Learning** | Perfect workshop project for AI-assisted development |
| 🎨 | **Customizable** | Swap questions, themes, scoring rules easily |

---

## 🚀 Get Started in 3 Steps

```bash
# 1️⃣  Clone & install
git clone https://github.com/copilot-dev-days/agent-lab-python.git
cd HackersMang2026
uv sync

# 2️⃣  Run mandatory checks
uv run ruff check .    # Lint
uv run pytest          # Test
uv run uvicorn app.main:app --reload --port 8001

# 3️⃣  Play! (http://localhost:8001)
```

---

## 🎮 How It Works

1. **Player joins** → Gets random bingo card questions
2. **Find matches** → Find people matching each question
3. **Mark the board** → Click squares as you find people
4. **Get bingo** → 5 in a row wins! (vertical, horizontal, or diagonal)

---

## 📚 Hands-On Workshop

Transform this into something amazing using **VS Code + GitHub Copilot**.

| Part | Topic | What You'll Build |
|------|-------|------------------|
| [**01**](workshop/01-setup.md) | Setup & Context | Teach AI about your codebase |
| [**02**](workshop/02-design.md) | Design-First UI | Redesign with custom themes |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | Your own question generator |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Build | New features with TDD |

**Full guides:** [workshop/](workshop/) folder or [online](https://copilot-dev-days.github.io/agent-lab-python/)

---

## 🛠️ Built With

- **Backend:** [FastAPI](https://fastapi.tiangolo.com/) — high performance async Python web framework
- **Templates:** [Jinja2](https://jinja.palletsprojects.com/) — powerful server-side templating
- **Frontend:** [HTMX](https://htmx.org/) — modern interactions without JavaScript chaos
- **Testing:** [pytest](https://pytest.org/) + [httpx](https://www.python-httpx.org/) — rock-solid tests
- **Code Quality:** [ruff](https://astral.sh/ruff/) — ultrafast Python linter

---

## 📊 Project Stats

- **25 tests** passing (100% coverage on game logic)
- **~800 lines** of clean Python code
- **<100ms** HTMX response times
- **Zero external JS** — just HTML, CSS, and smart interactions

---

## 🎯 Perfect For

✅ Learning FastAPI + HTMX in a real project  
✅ Understanding AI-assisted development workflows  
✅ Building social/event tech  
✅ Testing modern Python best practices  
✅ Workshop facilitators & dev teams  

---

## 🤝 Contributing

Want to improve Soc Ops? Jump in!

1. Fork this repo
2. Create a feature branch (`git checkout -b feature/amazing-thing`)
3. Follow the [dev checklist](#dev-checklist) (lint, test, build)
4. Commit your work
5. Open a PR

---

## 📋 Dev Checklist

Before any commit:

```bash
uv run ruff check .           # Lint
uv run pytest                 # Test  
uv run uvicorn app.main:app   # Build & Run
```

All must pass. [Full docs here](https://github.com/copilot-dev-days/agent-lab-python/blob/main/.github/instructions/workspace.instructions.md).

---

## 📖 Documentation

- [Workspace Instructions](.github/instructions/workspace.instructions.md) — dev setup & patterns
- [Workshop Guides](workshop/) — 5-part hands-on labs
- [API Reference](app/main.py) — routes & endpoints
- [Game Logic](app/game_logic.py) — scoring & bingo rules

---

## 🎓 What You'll Learn

- **Context Engineering** — Teach AI about your codebase
- **Design-First Development** — Iterate UI with AI guidance  
- **Test-Driven Development** — Build reliable features with tests first
- **Multi-Agent Workflows** — Coordinate specialized AI agents
- **Modern Python** — FastAPI, Jinja2, pytest best practices

---

## 📞 Support

- **Issues?** [GitHub Issues](https://github.com/copilot-dev-days/agent-lab-python/issues)
- **Questions?** Start with [Part 00](workshop/00-overview.md) or [online guide](https://copilot-dev-days.github.io/agent-lab-python/)
- **Contributing?** See [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

**Built with ❤️ for developers and AI enthusiasts. Happy coding! 🚀**
