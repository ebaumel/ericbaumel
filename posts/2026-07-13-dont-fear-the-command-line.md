---
title: "Don't Fear the Command Line"
description: The command line looks intimidating and isn't. A physician's guide to the ten commands that unlock everything else in coding and data science.
categories:
- development
date: '2026-07-13'
draft: true
toc: true
---

Remember the first time you scrubbed into a procedure?

A tray of instruments, most of which you couldn't name, and a room full of people who could. Two weeks later you knew the six you actually needed and reached for them without looking. The command line is the same tray. It looks like a wall of cryptic instruments, but the working set is small, and once you know it, everything in coding and data science opens up.

{{< video https://www.youtube.com/watch?v=f2ac-4fjSAE >}}

## Why bother with a text window in 2026?

Because it's where the tools live. Python environments, git, package installers, servers, every tutorial you'll ever follow: at some point they all say "open a terminal." If that sentence makes you close the tab, the command line is a wall. If it doesn't, it's a door.

There's a deeper reason too. The command line is precise. A click is an ambiguous gesture; a command is an order, written down, repeatable, and shareable. It's the difference between "give some pain medication" and a signed order with drug, dose, and route.

## The ten commands that do the work

Open Terminal on a Mac (or PowerShell on Windows; the ideas transfer) and try these. `$` just marks the prompt; don't type it.

```bash
pwd        # print working directory: "where am I?"
ls         # list what's in this folder
cd docs    # change directory into "docs" (cd .. goes up one level)
mkdir demo # make a new folder called "demo"
cp a.txt b.txt   # copy a file
mv a.txt archive/ # move (or rename) a file
rm b.txt   # remove a file (no trash can, no undo. Respect it like a scalpel.)
cat notes.txt    # print a file's contents to the screen
grep "fever" notes.txt  # search inside files for a word
man ls     # the manual page: the package insert for any command
```

That's the working set. `pwd`, `ls`, and `cd` are orientation: where am I, what's here, let's move. `mkdir`, `cp`, `mv`, and `rm` are the file operations you already do in Finder, just written as orders. `cat` and `grep` let you look inside files without opening anything. And `man` means you never have to memorize; the reference is always one command away.

## Try it yourself

Five minutes, no risk:

```bash
cd ~
mkdir practice
cd practice
echo "Hello from the command line" > hello.txt
cat hello.txt
```

You just created a folder, wrote a file, and read it back without touching the mouse. When you're done, `cd ..` then `rm -r practice` cleans it all up. (The `-r` removes a folder and its contents, so read twice, cut once.)

## Recap

The command line isn't a test you can fail. It's an instrument tray, and you now know the instruments that matter: three to orient, four to manage files, two to inspect, one to look things up. Watch the video, spend five minutes in the practice folder, and the next tutorial that says "open a terminal" won't slow you down at all.

Next step: with the terminal under your belt, my post on [putting your projects under source control](/posts/2021-01-03-git-init-2021.html) is the natural follow-on.

---

*__About the author:__ Eric M. Baumel, MD is a board-certified diagnostic radiologist, app developer, and digital health entrepreneur. He teaches technology to healthcare professionals at [Coding4Docs](https://www.youtube.com/@Coding4Docs). Read more on the [About page](/about.html).*
