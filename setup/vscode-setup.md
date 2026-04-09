# Setting Up Your Terminal in VSCode

*Last updated: April 2026*

You'll run your terminal agent from inside VSCode. This guide makes sure your terminal is ready.

## Why Use the VSCode Terminal?

Using the terminal inside VSCode means you can see your files in the sidebar while the agent works in the terminal panel at the bottom. When the agent creates or edits a file, you can open it immediately in the editor. Everything stays in one window.

## Step 1: Open a Folder in VSCode

1. Open VSCode
2. Go to **File > Open Folder**
3. Navigate to the `getting-started` folder in this repository and open it

**What you should see:** The VSCode sidebar shows the folder contents -- `setup/`, `exercises/`, `README.md`, etc.

## Step 2: Open the Terminal Panel

Use the keyboard shortcut:

```
Ctrl + `
```

(That's Ctrl plus the backtick key, usually above Tab on your keyboard.)

Or go to **View > Terminal** from the menu bar.

**What you should see:** A terminal panel appears at the bottom of VSCode. It should show a command prompt.

This guide assumes you're using **PowerShell**, which is the default terminal in VSCode on Windows. If your terminal shows something different (like `bash` or `cmd`), click the dropdown arrow (&#9662;) next to the **+** button in the terminal panel and select **PowerShell**.

## Step 3: Verify Your Agent Is Available

In the terminal panel, run the command for whichever agent you installed:

**For Codex:**
```
codex --version
```

**For Claude Code:**
```
claude --version
```

**What you should see:** A version number. If you see an error like "not recognized," close the terminal panel and reopen it (Ctrl + ` twice), or restart VSCode entirely. The terminal needs to pick up the PATH changes from your installation.

## Step 4: Verify the Repo Structure

Make sure your terminal is at the repo root (the `getting-started` folder you opened in Step 1). Run:

```
dir
```

**What you should see:** The top-level contents of the repo -- `exercises`, `setup`, `README.md`, etc. If you see these, the repo is properly set up and you're in the right place.

## You're Ready

Your terminal is set up inside VSCode and your agent is available. Head to the [exercise instructions](../exercises/01-summarize-folder/instructions.md) to start.
