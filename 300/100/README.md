# 100 - Installation

## Python Version

We recommend using the latest version of Python. (GitPod supports version 3.12.6 at the time of this writing).

## Virtual environments

Use a virtual environment to manage the dependencies for your project, both in development and in production.

What problem does a virtual environment solve? The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system’s packages.

Python comes bundled with the **[venv](https://docs.python.org/3/library/venv.html#module-venv)** module to create virtual environments.

### Create an environment

Create a project folder (here: ```app```) and a ```.venv``` folder within:

macOS/Linux:

```
$ mkdir app
$ cd app
$ python3 -m venv .venv
```

Windows:

```
> mkdir app
> cd app
> py -3 -m venv .venv
```

### Activate the environment

Before you work on your project, activate the corresponding environment:

macOS/Linux:

```
$ cd app
$ . .venv/bin/activate
```

Windows:

```
> cd app
> .venv\Scripts\activate
```

Your shell prompt will change to show the name of the activated environment.

To exit the environment use: ```exit```

## Install SpaCy

Within the activated environment, use the following command to install spaCy:

```
$ pip install spaCy
```

Alternatively, add ```spaCy``` to a requirements.txt file.

```
spacy>=2.1.2
```
app/requirements.txt

And install it like:

```
$ pip install -r requirements.txt
```

## Download and install languages

Within the activated environment, use the following command to install spaCy's language ```English```:

```
$ python -m spacy download en_core_web_sm
```