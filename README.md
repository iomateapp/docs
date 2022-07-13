# IOmate Developer Docs

The documentation was built using [MkDocs](https://www.mkdocs.org/), and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

## Prerequisites

Before proceeding with the next steps you need to have [Python3](https://www.python.org/downloads/) installed.

## Setup

Clone the project into your workspace

```bash
git clone https://github.com/iomateapp/docs.git
cd docs
```

### Virtual Environment
We suggest that you isolate the project in a [virtual environment](https://docs.python.org/3/library/venv.html) for better project management. you can do this by following the steps below:

```bash
python3 -m venv env
```

Activate the virtual environment to install the dependencies:

```bash
#Windows
./env/Scripts/Activate

# Linux / macOS
source ./env/bin/activate
```

### Installing dependencies

You can use the package manager [pip3](https://pip.pypa.io/en/stable/) to install project dependencies.

```bash
pip3 install -r requirements.txt
```

From now on you have the project ready to run locally.
MkDocs comes with a built-in dev-server that lets you preview your documentation as you work on it. Make sure you're in the same directory as the mkdocs.yml configuration file, and then start the server by running the mkdocs serve command:

```bash
mkdocs serve
```
