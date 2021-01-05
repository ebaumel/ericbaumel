# Setting up virtual environments in Python

This is an opinionated set of instructions to set up virtual environments for each project. 

After several other explorations, I use venv to manage the environments for my projects. 
Know that venv is not the only method of setting up virtual environments, 
but is the official suggested method by the folks at [python.org](https://docs.python.org/3/tutorial/venv.html).

There are several other methods, such as using the Anaconda Navigator or conda via the command line, pipenv and  pyenv.

## To get started:

Install python on computer, if this isn't already installed.

Check instillation of python on a clean Terminal window with `python —version` (that is a double dash).

Check instillation of pip with `pip —version`.

Install virtualenv with `pip install virtualenv`.

Check the instillation with `virtualenv —version`.

In your development directory of choice (ex.: the Desktop or /Dev or/Documents etc.). 

Create a new directory with `mkdir <Project_Name>`.

Navigate to the new project directory `cd <Project_Name>`.

Create a new env environment with `python -m venv venv`. 

Activate with `. venv/bin/activate` (don’t forget the ‘dot space’). You should see `(venv) ` before the terminal prompt confirming that you are in the active virtual environment.

Add new packages with `pip install ChosenPackage`.

Upgrade a package with `pip install --upgrade ChosenPackage`.

After installing dependencies use `pip freeze > requirements.txt` to list the requirements and version numbers for that project. For a clean install of all of these dependencies into another fresh environment, use `pip iinstall -r requirements.txt`

You can view the installed dependencies with `cat requirements.txt`.

Deactivate the virtual environment with `deactivate venv`.
