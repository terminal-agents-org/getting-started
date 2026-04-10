# Installing Claude Code

*Last updated: April 2026*

For the latest official instructions, see the [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code).

Claude Code is Anthropic's terminal-based coding agent. It runs on your machine, can read and write files, and responds to natural language instructions. This guide walks you through installing it on Windows.

## What You Need

- **Windows 10 or 11**
- **Git** installed ([download here](https://git-scm.com) if needed)
- **One of these:**
  - A Claude Pro or Max subscription (for OAuth sign-in)
  - An Anthropic API key (from console.anthropic.com)

## Step 1: Install Claude Code

Open PowerShell and run:

```powershell
irm https://claude.ai/install.ps1 | iex
```

This downloads and runs the native installer. It does not require Node.js.

> **Alternative:** If your organization blocks PowerShell install scripts, try `winget install Anthropic.ClaudeCode`.

**What you should see:** The installer will download Claude Code and set up the `claude` command. If Git is not installed, it will prompt you to install it first.

> **Important:** After the installer finishes, **close your terminal and open a new one**. The PATH changes need a fresh terminal to take effect.

**Verify it worked:**

```
claude --version
```

You should see a version number printed.

> **Alternative install method:** If you already have Node.js 18+ installed, you can also install via npm: `npm install -g @anthropic-ai/claude-code`. However, the native installer above is Anthropic's recommended method.
>
> **Note:** Anthropic has deprecated the npm install method. Use the native installer above instead. The npm method still works but may not receive future updates.

## Step 2: Sign In

Run Claude Code for the first time:

```
claude
```

Claude Code will open a sign-in page in your browser where you log in with your claude.ai account. After you approve in the browser, the terminal will confirm authentication succeeded.

**What you should see:** Claude Code confirms it's authenticated and shows you an interactive prompt.

> **Alternative (API key):** If you prefer to use an API key, set it as an environment variable before running Claude Code:
> ```powershell
> $env:ANTHROPIC_API_KEY = "your-key-here"
> claude
> ```
> You can get an API key from [console.anthropic.com](https://console.anthropic.com) under API Keys.

## Step 3: Verify Everything Works

Navigate to any folder and run:

```
claude "What files are in this directory?"
```

**What you should see:** Claude Code will list the files in your current directory. If it responds with a file listing, your installation is working.

## Troubleshooting

**"claude is not recognized"**
- Close your terminal and open a new one. The PATH update from the installer needs a fresh terminal.
- If it still doesn't work, try running the installer again.

**Authentication fails**
- Make sure your Claude subscription is active at [claude.ai](https://claude.ai).
- Start Claude Code by running `claude`, then type `/login` at the Claude Code prompt (not in your regular terminal).

**Git-related errors**
- Claude Code on Windows requires Git for Windows (which includes Git Bash) or WSL. You can launch `claude` from PowerShell, CMD, or Git Bash. Install Git from [git-scm.com](https://git-scm.com) if you don't have it.

## Next Step

Head to the [VSCode setup guide](vscode-setup.md) to configure your terminal inside your editor, then start the first exercise.
