---
aliases:
- /claude/development/2026/25/05/claude-code-end-of-session-ritual
- /posts/2026-25-05-claude-code-end-of-session-ritual.html
author: Eric M. Baumel
categories:
- claude
- development
date: '2026-05-25'
description: A Claude Code skill - `/wrapup` — a five-step end-of-session ritual that takes about five minutes and closes out a session properly.
layout: post
title: Claude Code End-of-Session Ritual
toc: false
---


Every Claude Code session starts with amnesia.

You want to pick up where you left off, but you need to explain the project all over again or waste tokens having Claude look at the file structure. I would spend the first ten minutes re-explaining what I was doing, what I had already decided, and what the actual next step was.

Claude Code is a blank slate at the start of every session. It doesn't remember that I chose Firebase over CloudKit for HIPAA reasons. It doesn't know I already solved the anonymous auth problem. It has no idea what I was about to do next.

For a while I just lived with that friction. Then I got tired of it and built a fix.

Each session is a fresh context window. So the question is: *how do I make sure the right context is always written down in a place Claude reads automatically?*

The answer is for Claude Code to read the `CLAUDE.md` at the start of every session. If that file has a clear, present-tense description of where the project is right now and exactly what comes next, the session starts in five seconds instead of ten minutes. It's less like a memory and more like a standing briefing doc.

## What I Built

I created a Claude skill called `/wrapup` — a five-step end-of-session ritual that takes about five minutes and closes out a session properly. You can find it here for free on GitHub [claude-wrapup](https://github.com/ebaumel/claude-wrapup).

Here's what it does:

**Step 1: Brain Dump.** Before touching any files, it reads the git diff from the session and asks: *does this capture what you did today, or is there anything to add?* You might think of this as an answer to four questions: what did I complete, what's still in progress, what's the single next action, and were there any non-obvious decisions?

**Step 2: Update `CLAUDE.md`.** It proposes specific edits and waits for confirmation before writing. The file stays present-tense and forward-looking — a briefing doc, not a changelog.

**Step 3: Update `DECISIONS.md`.** Any architectural choices from the session get logged as a new append-only entry. This file never gets edited or deleted. Six months from now, when you're wondering why you chose X over Y, this file is the answer.

**Step 4: Commit to Git — with a `Next:` line.** It drafts a conventional commit message from the session summary. The key addition is a `Next:` line at the bottom of the commit message that states the single immediate next action. Your git log becomes a resumption guide.

**Step 5: Update Claude Memory.** Claude Code can't write directly to your Claude.ai memory, so the skill ends with a pre-filled copy-paste block you can drop into your Claude.ai chat to keep cross-project memory current.

Now, when you want to pick a project back up, just type `claude`.

---

The `DECISIONS.md` pattern deserves its own callout, because it is a gift for future you.

When you're building something over weeks or months, you make dozens of small architectural decisions. Some are obvious in retrospect. Others only made sense given constraints that existed at the time, and if you forget those constraints, the decision looks arbitrary or even wrong.

In medicine, we document our clinical reasoning in the patient's chart, not just our orders. The note captures *why* we chose this medication, not just that we chose it. `DECISIONS.md` is that note for your codebase. And because it's append-only, you never accidentally overwrite history.

## The Bigger Picture

Every session you end without a proper close is a small tax on the next one. Multiply that by fifty sessions on a project and you've spent hours just getting back up to speed.

### Please give it a try: [claude-wrapup](https://github.com/ebaumel/claude-wrapup)


The `/wrapup` ritual makes each session a clean handoff to the next one. For anyone building something real with Claude Code — especially those of us doing it without a team around us — that's worth five minutes at the end of every session.

---

*__About the author:__ Eric M. Baumel, MD is a board-certified diagnostic radiologist, app developer, and digital health entrepreneur. He teaches technology to healthcare professionals at [Coding4Docs](https://www.youtube.com/@Coding4Docs). Read more on the [About page](/about.html).*
