# MLOPS_experience

## Setup environment

To ensure there is no conflict in term of dependency, it is recommened to use **Poetry** as Python dependency management framework.

1. Install dependencies

If your project already has a `pyproject.toml` file, install the dependencies by running:

```bash
poetry install
```

2. Activate the virtual environment

```bash
poetry shell
```

3. Manage dependencies

* To add a package

```bash
poetry add package_name
```

* To remove a package

```bash
poetry remove package_name
```

* To update dependencies

```bash
poetry update 
```

## Training
