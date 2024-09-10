---
aliases:
- /html/development/2024/09/09/Firebase-hosting-deployment
author: Eric M. Baumel
categories:
- html
- development
date: '2021-09-09'
description: Adding to you GitHub Pages blog ith Jupyter Notebooks or Markdown generated HTML *à la* Fastpages using Quarto.
layout: post
title: Publishing a GitHub Pages Blog with Quarto
toc: false
---

## GitHub Pages Blog with Quarto


Inspired by the fastpages blogs

nbdev and Quarto an [End-To-End Walkthrough
](https://nbdev.fast.ai/tutorials/tutorial.html#install-nbdev)

From Christian Wittmann  - [How I created this Blog](https://chrwittm.github.io/posts/2022-10-21-how-i-created-this-blog/)


Install the Quarto extension for VS Code.

You can preview on your local system with

`quarto preview <full/path/file.name> --no-browser --no-watch-inputs`

When you run 

`quarto publish gh-pages`

 your blog posts are rendered, and the rendered versions are pushed to git in branch *gh-pages*

To backup your local copy of the unrendered files, save to the git main branch. For details see the GitHub cheatsheet, [git init 2021]( https://www.ericbaumel.com/posts/2021-01-03-git-init-2021.html)



[Markdown Cheat Sheet(]https://www.markdownguide.org/cheat-sheet/)



