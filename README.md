# Getting Started with Terminal Agents

## What You'll Learn

This module takes you from zero terminal agent experience to completing your first real task with one. A terminal agent is an AI assistant that runs inside your computer's command line (terminal) instead of in a browser window. By the end, you'll have a working terminal AI agent and you'll have used it to do something that browser-based AI chat (like ChatGPT in a browser) can't do nearly as easily: read multiple files on your computer and produce a new file from them.

**Why this matters:** In browser chat, you'd need to open each file, copy its contents, paste them into the chat window, then copy the response back into a new file. A terminal agent reads and writes files directly on your machine. The difference becomes obvious the moment you try it.

## Prerequisites

Before starting, make sure you have:

- **VSCode** installed on your computer
- **Git** installed ([git-scm.com](https://git-scm.com)) -- needed to clone this repository (and for the Claude Code path)
- **One of these subscriptions:**
  - An OpenAI subscription (Plus, Pro, or higher) for Codex -- this is the recommended path
  - Anthropic API key or Claude Pro/Max subscription (for Claude Code)
- **Node.js 22 or newer** (needed for Codex -- download from [nodejs.org](https://nodejs.org) if you don't have it; not needed for the Claude Code path)
- **Willingness to try the command line** -- no prior experience needed, we'll walk you through every step

> **No Git?** If you're following the **Codex path**, you can download this repository as a ZIP file from the green "Code" button on the [GitHub page](https://github.com/terminal-agents-org/getting-started) and extract it. Note: the extracted folder will be named `getting-started-main` — rename it to `getting-started` so the instructions match. (The **Claude Code path** requires Git, so you'll need to install it first.)

## How to Use This Module

### 1. Clone this repository

Open a terminal (PowerShell) and navigate to a folder where you want to keep your learning materials. Then run:

```
git clone https://github.com/terminal-agents-org/getting-started.git
```

This creates a `getting-started` folder in your current location. Open it in VSCode: use **File > Open Folder** and select the `getting-started` folder.

> **Tip:** If you have the VSCode `code` command on your PATH, you can also run `code getting-started` from the terminal.

### 2. Choose Your Agent

| Agent | Best if you have... | Setup guide |
|-------|---------------------|-------------|
| **Codex** (recommended) | OpenAI Pro subscription | [Install Codex](setup/install-codex.md) |
| **Claude Code** | Anthropic API key or Claude subscription | [Install Claude Code](setup/install-claude.md) |

Both agents can complete every exercise in this module. We recommend Codex as the primary path since most learners in this program have OpenAI Pro access.

### 3. Set Up Your Editor

Follow the [VSCode setup guide](setup/vscode-setup.md) to configure your terminal inside VSCode. This is where you'll run the agent.

### 4. Complete the Exercise

Head to the exercise folder and follow the instructions:

- [Exercise 1: Summarize a Folder](exercises/01-summarize-folder/instructions.md)

The exercise includes seed files for the agent to work with and an expected output so you can compare your results.

## Module Structure

```
getting-started/
  setup/
    install-codex.md        # Codex installation guide
    install-claude.md       # Claude Code installation guide
    vscode-setup.md         # VSCode terminal setup
  exercises/
    01-summarize-folder/
      instructions.md       # What to do
      seed-files/           # Files the agent will read
      expected-output/      # What good output looks like
```

## Getting Help

If you get stuck:

1. Re-read the step you're on -- each step has a verification check
2. Ask your terminal agent for help (that's what it's there for)
3. Check the expected output to see what you're aiming for
4. Reach out to the learning community
