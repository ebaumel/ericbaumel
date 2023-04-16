---
aliases:
- /python/data science/development/2021/01/04/Setting-up-virtual-environments-in-python
author: Eric M. Baumel
categories:
- python
- data science
- development
date: '2021-01-04'
description: A receipe for setting up a virtual environment for Python projects.
layout: post
title: Setting Up Virtual Environments in Python
toc: false

---

## A Clean, Well-Lighted Place


> This is an opinionated set of instructions to set up virtual environments for each project. 

A virtual environement is a clean sandbox without any installed python libraries. This allows you to add the libraries you need for your project, without conflicts from packages installed for other, unrelated projects on your system. This also helps you containerize you projects so they can be deployed cleanly or shared with other developers.

After several other explorations, I use venv to manage the environments for all my projects. 
Know that venv is not the only method of setting up virtual environments, 
but is the officially suggested method by the folks at [python.org](https://docs.python.org/3/tutorial/venv.html).

There are several other methods, such as using the Anaconda Navigator or conda via the command line, pipenv and pyenv.

### To get started:

* Install Python on computer, if this isn't already installed.

* Check instillation of Python on a clean Terminal window with `python —version` _(that is a double dash)_.

* Check instillation of pip with `pip —version`.

* Install virtualenv with `pip install virtualenv`.

* Confirm the instillation with `virtualenv —version`.

* In your development directory of choice (ex.: the Desktop, /Dev, /Documents, etc.), create a new directory with `mkdir <Project_Name>`.

* Navigate to the new project directory `cd <Project_Name>`.

* Create a new env environment with `python -m venv venv`. 

* Activate with `. venv/bin/activate` _(don’t forget the ‘dot space’)_. You should see `(venv) ` before the terminal prompt, confirming that you are in the active virtual environment.

* Add new packages with `pip install SomePackage`.

* Upgrade a package with `pip install --upgrade SomePackage`.

* After installing dependencies, use `pip freeze > requirements.txt` to list the requirements and version numbers for that project. For a clean install of all of these dependencies into another fresh environment, use `pip install -r requirements.txt`

> You can view the installed dependencies with `cat requirements.txt`.

* Deactivate the virtual environment with `deactivate venv`.



