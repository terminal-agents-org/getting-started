# Exercise 1: Summarize a Folder

## Goal

Use your terminal agent to read all the files in a folder and produce a single summary document. This is the kind of task where a terminal agent clearly outshines browser-based AI chat -- instead of copying and pasting each file into a chat window, the agent reads everything directly from your file system and writes the result back.

## What You'll Do

Ask your agent to read the three files in the `seed-files/` folder and create a `summary.md` file that pulls together the key information from all of them.

## The Seed Files

Take a quick look at the files in `seed-files/` before you start:

- **meeting-notes.txt** -- notes from a fictional team meeting
- **tasks.csv** -- a small table of tasks with status and priority
- **ideas.txt** -- a brainstorm list of project ideas

You can open them in VSCode to see what's in each one. They're short -- under a minute to read.

## Instructions

### 1. Open your terminal in VSCode

Make sure you're in the exercise folder. From the `getting-started` root:

```
cd exercises/01-summarize-folder
```

Run `dir` (or `ls`) to confirm you see the `seed-files/` and `expected-output/` folders before continuing.

### 2. Run your agent

**If you're using Codex:**
```
codex "Read all the files in the seed-files/ folder and create a summary.md that synthesizes the key information from each file."
```

**If you're using Claude Code:**
```
claude "Read all the files in the seed-files/ folder and create a summary.md that synthesizes the key information from each file."
```

### 3. Watch what happens

The agent will:
1. Read each file in the folder
2. Analyze the content
3. Create a new `summary.md` file

You may see the agent ask for permission to read files or create the new file. **Approve these actions** -- when prompted, type `y` and press Enter (or click Allow). These permission checks are a safety feature that lets you stay in control.

**Codex users:** Codex runs in 'suggest' mode by default -- it will show you each action and wait for your approval. Press Enter or type `y` to approve each step. This is normal and expected for your first run.

### 4. Check the result

After the agent finishes, open the newly created `summary.md` file in VSCode. It should contain a coherent summary that references information from all three source files.

### 5. Compare with the expected output

Open `expected-output/summary.md` in VSCode (click it in the sidebar) to see an example of what a good summary looks like. Your agent's output won't match word-for-word (that's fine -- every run produces slightly different wording), but it should cover the same key points.

## What to Look For

A good summary should:

- Mention the project discussed in the meeting notes
- Reference the task statuses from the CSV
- Include the brainstormed ideas
- Be organized and easy to read
- Synthesize (combine and connect), not just list each file's contents separately

## Why This Matters

Think about what you just did compared to how you'd do this in browser chat:

| Browser Chat | Terminal Agent |
|-------------|---------------|
| Open file 1, copy contents, paste into chat | Agent reads all files directly |
| Repeat for file 2 and file 3 | (done automatically) |
| Copy the response from chat | Agent writes the file for you |
| Create a new file, paste contents | (already on disk) |
| 6+ manual steps | 1 command |

This is a simple example, but the principle scales. Imagine doing this across 50 files, or an entire codebase. That's where terminal agents transform your workflow.

## Done?

Congratulations -- you've completed your first terminal agent exercise. You've installed an agent, used it to process multiple files, and seen the result appear directly on your machine.

## What's Next

You've completed the first module. Here are some ideas:

- **Explore on your own:** Try asking the agent to do something else with the seed files -- reformat the CSV, find action items, or generate a to-do list.
- **Browse more modules:** Return to the [Terminal Agents Learning Platform](https://github.com/terminal-agents-org) to see what's available.
- **Next module:** *Coming soon* -- we'll link the next module here when it's ready.
