# Nextflow cookiecutter template

Cookiecutter template for creating new [Nextflow](https://www.nextflow.io/) pipelines.

Use this template on your own machine with cookiecutter, or create a brand new repository based on this template entirely through the GitHub web interface using [nextflow-template-repository](https://github.com/Arcadia-Science/nextflow-template-repository).

This is fully inspired by the following blog post: https://simonwillison.net/2021/Aug/28/dynamic-github-repository-templates/. The README instructions here are modified from [this GitHub repository](https://github.com/simonw/click-app).

## Installation via GitHub templates

You can start [here](https://github.com/Arcadia-Science/nextflow-template-repository/generate) and follow the prompts.

## Installation locally

You'll need to have [cookiecutter](https://cookiecutter.readthedocs.io/) installed.

```{bash}
pip install cookiecutter
```

## Usage

Run `cookiecutter gh:Arcadia-Science/nextflow-template` and then answer the prompts. Here's an example run:

```{bash}
$ cookiecutter gh:simonw/click-app
```

It is strongly recommended to accept the suggested value for "hyphenated" and "underscored" by hitting enter on those prompts.

Having created the new structure from the template, here's how to start working on the tool.

If your tool is called `my-new-tool`, you can start working on it like so:

    cd my-new-tool
    # Create and activate a virtual environment:
    python3 -m venv venv
    source venv/bin/activate
    # Install dependencies so you can edit the project:
    pip install -e '.[test]'
    # With zsh you have to run this again for some reason:
    source venv/bin/activate
    # Confirm your tool can be run from the command-line
    my-new-tool --version

You should see the following:

    my-new-tool, version 0.1

You can run the default test for your tool like so:

    pytest

This will execute the test in `tests/test_my_new_tool.py`.

Now you can open the `my_new_tool/cli.py` file and start adding Click [commands and groups](https://click.palletsprojects.com/en/7.x/commands/).

## Creating a Git repository for your tool

You can initialize a Git repository for your tool like this:

```{bash}
cd my-new-tool
git init
git add .
git commit -m "Initial structure from template"
# Rename the 'master' branch to 'main':
git branch -m master main
```

## Publishing your tool to GitHub

Use https://github.com/new to create a new GitHub repository sharing the same name as your tool, which should be something like `my-new-tool`.

Push your `main` branch to GitHub like this:

```{bash}
git remote add origin git@github.com:YOURNAME/my-new-tool.git
git push -u origin main
```
