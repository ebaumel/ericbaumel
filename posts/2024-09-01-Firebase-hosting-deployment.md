---
aliases:
- /html/development/2024/09/01/Firebase-hosting-deployment
author: Eric M. Baumel
categories:
- html
- development
date: '2021-09-01'
description: A receipe for deploying your website to Firebase Hosting.
layout: post
title: Firebase Hosting Deployment
toc: false

---

by Eric M. Baumel

## Deploying your website on Firebase Hosting

> This is another of a series of mini-posts, mostly cheatsheets for my own use. Maybe of some value for others.


### Firebase Hosting Deployment


Update the website in your text editor of choice, such as VSCode.


Open the Terminal and navigate to the directory containing the website.

`npm install firebase`

`firebase init hosting`

If you get a “Failed to get Firebase project *\<project name\>*. Please make sure the project exists and your account has permission to access it.” error message run 
 
`firebase logout`

Followed by

`firebase login`


Firebase will then ask you to login to your account on your browser. After authentication you will be able to log in.


`firebase init hosting`

Firebase will ask a few setup question.

What do you want to use as your public directory? *public*

Configure as a single-page app (rewrite all urls to /index.html)? *No*

Set up automatic builds and deploys with GitHub? No

If you already have a deployment for this project, it will ask if you want to overwrite your 404.html and index.html files.

`firebase serve`

Will setup a local test server on you computer at http://localhost:5002 where you can view your site before deployment.


Deploy the site to the Firebase Hosting server with
`firebase deploy`

After you are done editing your deployment, don’t forget to save your changes to GitHub.

