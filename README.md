### Summary

This repo was set up to demonstrate how to build, share, and package a kivy python project using pipenv for package management and pyinstaller for bundling. It is using the basic kivy pong tutorial available on the kivy website: [Kivy Pong Tutorial](https://kivy.org/doc/stable/tutorials/pong.html). This project contains the source for the kivy pong app and instructions to package it into a executable for Windows.

---

### Set Up

#### Ensure Correct Version of Python

This project requires a specific version python to run properly. Reference the required version in this project's <em>Pipfile</em> and ensure that it is installed on your system ([Python Downloads](https://www.python.org/downloads/)). It is not required to be the default python install, it just needs to be present. Take note of its install location to use later.

#### Install Pipenv

This project uses pipenv for dependency and environment management.

From a terminal run: `pip install pipenv`. Detailed installation instructions can be found here: [Installing Pipenv](https://pipenv.pypa.io/en/latest/install/#installing-pipenv).

#### Download Source Code and Set Up Local Environment

With pipenv, create a virtual environment in the project's directory using the required python version.

1. Clone this repository: `git clone https://github.com/CaseyMatthews/kivy-pong-tutorial.git`

2. Navigate to the project directory.

3. Initialize the pipenv virtual environment: `pipenv install --dev --python path/to/python/install/python.exe`. Replace the path with python's install location as previously noted.

4. Install missing Kivy dependency (required for bundling): `pipenv install kivy_deps.sdl2`

##### Note for IDEs
If your IDE is not resolving packages installed via pipenv, then you may need to configure it to use the python interpreter inside the pipenv virtual environment.

<em>vscode:</em> `CTRL + SHIFT + P`, `>Python select interpreter`

---

### Basic Usage

#### Package and Environment Management

| Pipenv Operation                                               | Command                 |
|----------------------------------------------------------------|-------------------------|
| Create a new project using Python 3.7, specifically            | `pipenv --python 3.7`   |
| Remove project virtualenv (inferred from current directory)    | `pipenv --rm`           |
| Install all dependencies for a project (including dev)         | `pipenv install --dev`  |
| Create a lockfile containing pre-releases                      | `pipenv lock --pre`     |
| Show a graph of your installed dependencies                    | `pipenv graph`          |
| Check your installed dependencies for security vulnerabilities | `pipenv check`          |
| Install a local setup.py into your virtual environment/Pipfile | `pipenv install -e .`   |
| Use a lower-level pip command                                  | `pipenv run pip freeze` |

#### Run the App

Terminal: `python main.py`

#### Build the App

Terminal: `python -m PyInstaller Pong.spec`

If pyinstaller complains about missing kivy dependencies, you may need to install explicitly to your virtual environment (e.g. `pipenv install kivy_deps.sdl2`).

If the build was successful, there will be a <em>Pong.exe</em> file in the<em>dist/</em>.