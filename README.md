# know-nothing

Agent skill that helps you learn what you are doing while doing it.

## Why

AI tools can do almost everything for you. That's useful, and it quietly takes away the best part of learning: the "aha" moment, when after studying and trying you finally use new knowledge to solve a problem *and understand why it worked*. That small step makes you hungry for the next one ("what if I made a better version?"), and the cycle keeps growing.

`know-nothing` keeps that moment yours. You say what you want to do. The skill finds out what you already know, then guides you through it as a series of **micro challenges**. It never gives lectures and never does the work for you.

## How it works

1. **You name a goal:** `/know-nothing build a CLI todo app in Python`
2. **It asks what you already know**, one question at a time, so the steps fit you.
3. **You get a quest map** of 3–8 small steps.
4. **Each step is a challenge.** To move on, answer **3 questions** about the step correctly, or **show proof** you did it (a file, code, a link, command output). Skipping is always allowed, it's just not the default.
5. **Wrong answer?** You get a hint, not the answer, then a fresh question.
6. **It pushes back.** If you sound too sure, or now and then even when you're right, it challenges you to prove it wasn't luck. It never says a right answer is wrong.
7. **Every step comes with optional resources:** videos, docs, articles, to dig deeper if you want.
8. **Progress is saved** in `.know-nothing/journey.md`, so you can stop and resume later.

It works for anything learnable, not just code. It replies in the language you write in.

## Install

### Claude Code

```bash
git clone https://github.com/<your-user>/know-nothing ~/.claude/skills/know-nothing
```

Working on the skill locally? Link the folder instead:

```bash
ln -s "$(pwd)" ~/.claude/skills/know-nothing
```

Start a new session and type `/know-nothing`.

### Claude.ai

Zip this folder and upload it under Settings → Skills.

## Use

```
/know-nothing <what you want to build or learn to do>
```

Without a goal, it resumes your last journey if one exists, or asks what you'd like to learn.

## A taste of it

```
you:    /know-nothing write a script that renames my photos by date
claude: Fun one! Before we start: have you written any scripts before, in any language?
you:    a bit of Python
claude: Nice. Have you ever read or touched file names from code?
you:    no
claude: Perfect, we'll start there. 🗺️ Here's the map: 1) See your files · 2) Read a photo's date · 3) Build a new name · 4) Rename safely · 5) Do it for a whole folder
        Step 1: write a few lines that print every file name in a folder. If you'd like a hand:
        📄 official docs · the "pathlib" module: the modern way to list files
        Show me what you come up with!
```

## Layout

```
SKILL.md                      the core loop
references/challenge-craft.md steps, questions, judging, pushback
references/hint-ladder.md     what to do when you're stuck
references/resources.md       how learning resources are chosen and checked
references/journey-template.md  the progress file
```
