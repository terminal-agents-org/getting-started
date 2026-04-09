# Installing Codex CLI

*Last updated: April 2026*

For the latest official instructions, see the [OpenAI Codex CLI documentation](https://github.com/openai/codex).

Codex is OpenAI's terminal-based coding agent. It runs on your machine, can read and write files, and responds to natural language instructions. This guide walks you through installing it on Windows.

## What You Need

- **Windows 10 or 11**
- **Node.js 22 or newer** (we'll check this below)
- **An OpenAI Pro subscription** (Plus, Pro, Business, Edu, or Enterprise all work)

## Step 1: Check if Node.js Is Installed

Open a terminal (PowerShell or Windows Terminal) and run:

```
node --version
```

**What you should see:** A version number like `v22.x.x` or higher.

**If you see an error** or the version is below 22, install Node.js from [nodejs.org](https://nodejs.org). Download the LTS version (make sure it is version 22 or higher), run the installer, then close and reopen your terminal and check again.

## Step 2: Install Codex CLI

Run this command in your terminal:

```
npm install -g @openai/codex
```

**What you should see:** npm output showing the package was installed. It may take a minute.

> **Important:** The package name is `@openai/codex` -- not just `codex`. There is a different, unrelated package called `codex` on npm.

**Verify it worked:**

```
codex --version
```

You should see a version number printed.

## Step 3: Sign In to Your OpenAI Account

Run Codex for the first time:

```
codex
```

Codex will prompt you to sign in. Choose **Sign in with ChatGPT** (recommended). This will open a browser window where you complete the login flow with your OpenAI account.

**What you should see:** After signing in through the browser, the terminal will confirm that authentication was successful. Codex caches your login so you won't need to do this again.

> **Alternative:** You can also sign in with an OpenAI API key if you prefer, but signing in with your ChatGPT account is the simplest path if you have a Pro subscription.

## Step 4: Verify Everything Works

Navigate to any folder and run:

```
codex "What files are in this directory?"
```

**What you should see:** Codex will list the files in your current directory. If it responds with a file listing, your installation is working.

## Troubleshooting

**Windows users:** Codex CLI on Windows is currently labeled experimental by OpenAI. Most users will have no issues, but if you run into problems, consider using [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) as an alternative -- note that WSL setup requires some additional effort.

**"codex is not recognized"**
- Close your terminal and open a new one. The PATH update from npm may need a fresh terminal.
- Make sure you used `npm install -g` (the `-g` flag installs it globally).

**Authentication fails**
- Make sure your OpenAI subscription is active at [platform.openai.com](https://platform.openai.com).
- Try running `codex login` to re-authenticate.

**npm permission errors**
- Run PowerShell as Administrator (right-click > "Run as administrator") and try the install command again.

## Next Step

Head to the [VSCode setup guide](vscode-setup.md) to configure your terminal inside your editor, then start the first exercise.
