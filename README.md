### Summary

This repo was set up to demonstrate how to build, share, and package a kivy python project using pipenv for package management. It is using the basic kivy pong tutorial available on the kivy website: [Kivy Pong Tutorial](https://kivy.org/doc/stable/tutorials/pong.html).

---

### Set Up

#### Ensure Correct Version of Python

This project requires a specific version python to run properly. Reference the required version in this project's <em>Pipfile</em> and ensure that it is installed on your system ([Python Downloads](https://www.python.org/downloads/)). It is not required to be the default python install on your system, it just needs to be present. Take note of its install location to use later.

#### Install Pipenv

This project uses pipenv for dependency and environment management.

From a terminal run: `pip install pipenv`. Detailed installation instructions can be found here: [Installing Pipenv](https://pipenv.pypa.io/en/latest/install/#installing-pipenv).

#### Download Source Code and Set Up Local Environment

With pipenv, create a virtual environment in the project's directory using the required python version.

1. Clone this repository: `git clone https://github.com/CaseyMatthews/kivy-pong-tutorial.git`

2. Navigate to the project directory.

3. Initialize the pipenv virtual environment: `pipenv install --python path/to/python/install/python.exe`. Replace the path with python's install location as previously noted.

##### Note for IDEs
If your IDE is not resolving packages installed via pipenv, then you may need to configure it to use the python interpreter inside the pipenv virtual environment.

vscode: <em>\<ctrl\> + \<shift\> + p</em> -> `>Python select interpreter`

---

### Basic Usage

##### Start Pipenv Virtual environment
`pipenv shell`

##### Stop Pipenv Virtual environment
`exit`

##### Install Packages
`pipenv install <package-name>`

##### Update Packages
You can manually alter <em>Pipfile</em> then run `pipenv install`