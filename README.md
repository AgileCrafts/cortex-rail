# Cortex Rail

**An operating system for AI software development, with a free desktop app to run it.**

AI coding agents are fast, and they drift fast. They skip the plan, forget what was decided last week, and change things nobody asked for. Cortex Rail puts them on a rail: they plan first, wait for your approval, build one task at a time, and share a project memory that never forgets.

It works with the AI tools you already use. It is free.

---

## Install

**Windows** — paste into PowerShell:

```powershell
irm https://github.com/AgileCrafts/agent-os-dashboard-dist/releases/latest/download/install.ps1 | iex
```

**Linux** — paste into a terminal:

```sh
curl -fsSL https://github.com/AgileCrafts/agent-os-dashboard-dist/releases/latest/download/install.sh | sh
```

Both install into your own folders, need no administrator rights, check the download against its published fingerprint, and add Cortex Rail to your app menu. The app keeps itself up to date.

Already have Node.js? `npx @agilecrafts/agent-os-dashboard` works too.

## How it works

1. **Open a project.** Pick any folder. Cortex Rail adds a small set of rules to it — plain text files your AI tools read.
2. **Say what you want.** Describe the product in the chat. Your AI asks its questions in plain words and writes the plan.
3. **Approve.** Nothing touches your code until you say yes. This is a lock, not a polite request: the AI is blocked from writing code before your approval.
4. **Build.** The AI works through the task list one task at a time. You watch the board move and can stop, steer or take over at any point.
5. **Come back any time.** Tomorrow, next month, on another computer or with a different AI — the project remembers where things stand and why.

## What you get

**Everything from one chat**
Start work, approve plans, check progress and answer the AI's questions from a single chat, in plain words. No commands to memorise.

**A plan before any code**
Requirements, questions, a plan and a task list come first. The amount of process scales with the project: a quick demo stays light, a serious product gets the full treatment.

**Approval that can't be skipped**
Code is locked until you approve the task list. The lock is enforced by the tools themselves, so an AI can't talk its way around it.

**Memory that never forgets**
- Decisions, lessons and pitfalls are saved as short notes inside your project.
- Before each message, the notes that matter are found by meaning and handed to the AI — it doesn't re-read everything, and you don't repeat yourself.
- The search runs on your own computer. Your notes are not sent anywhere to be searched.
- Notes that may be out of date are flagged, so the AI checks the code before trusting them.
- When a task is done, the AI writes down what it learned. Every save can be undone.

**Lower AI bills**
Each step loads only what it needs instead of the whole project history, and old notes are tidied away automatically. Long projects stay cheap to work on.

**Many AIs, one project**
Use Claude Code, Codex, OpenCode, Gemini CLI, Qwen Code, Cursor CLI, GitHub Copilot CLI or Aider — and mix them. Each can take the step it is best at, and they all follow the same rules and share the same memory. Cortex Rail finds the ones you have installed; you choose.

**Built for teams**
See who is on which task, get a heads-up before two people collide, and pick up where a teammate stopped from a short handoff note.

**A live view of the work**
A task board that updates as the AI works, terminals you can watch or type into, and a list of every change made to your code.

**Yours, on your computer**
Cortex Rail runs locally. There is no Cortex Rail account and no Cortex Rail server holding your code. Your AI tools keep using their own sign-ins.

## What gets added to your project

Opening a project adds a folder of rules (`.agent-os/`), a `documents/` folder for the plan, the task list and the memory notes, and small pointer files your AI tools look for. They are plain text. Read them, keep them in git with the rest of your project, and change the rules to suit how you work.

## Requirements

- Windows 10 or 11 (64-bit), or 64-bit Linux (Ubuntu 20.04+, Debian 11+, Fedora 34+ and similar).
- At least one AI coding tool installed and signed in. Cortex Rail can help you install and sign in to the supported ones.

## Updating and removing

The app tells you when a new version is ready and updates itself.

Remove on Windows:

```powershell
& ([scriptblock]::Create((irm https://github.com/AgileCrafts/agent-os-dashboard-dist/releases/latest/download/install.ps1))) -Uninstall
```

Remove on Linux:

```sh
curl -fsSL https://github.com/AgileCrafts/agent-os-dashboard-dist/releases/latest/download/install.sh | sh -s -- --uninstall
```

Your projects are never touched.

## Problems and ideas

Found a bug or want something added? [Open an issue](../../issues). Say what you did, what you expected and what happened; a screenshot helps.

## License

Cortex Rail is free to use, for personal and commercial work. The app itself is not open source. The rules it adds to your projects are yours to read and change. See [LICENSE.md](LICENSE.md).

Made by [AgileCrafts](https://agilecrafts.com).
