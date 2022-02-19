### Summary

This repo was set up to demonstrate how to build, share, and package a kivy python project using pipenv for package management. It is using the basic kivy pong tutorial available on the kivy website: [Kivy Pong Tutorial](https://kivy.org/doc/stable/tutorials/pong.html).

---

### Set UP

#### Install Pipenv

This project uses pipenv for dependency and environment management.

From a terminal run: `pip install pipenv`. Detailed installation instructions can be found here: [Installing Pipenv](https://pipenv.pypa.io/en/latest/install/#installing-pipenv).

#### Download Source Code and Set Up Local Environment

1. Clone this repository: `git clone https://github.com/CaseyMatthews/kivy-pong-tutorial.git`

2. Navigate to the project directory.

3. Initialize the pipenv virtual environment: `pipenv shell`.

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