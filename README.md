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

Run `cookiecutter gh:Arcadia-Science/nextflow-template` in your terminal and then answer the prompts. Here's an example run:

```{bash}
cookiecutter gh:Arcadia-Science/nextflow-template
```

It is strongly recommended to accept the suggested value for "hyphenated" and "underscored" by hitting enter on those prompts.

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

## Citations
This cookiecutter template is based off of the `nf-core` template. You can cite the `nf-core` publication as follows:
> **The nf-core framework for community-curated bioinformatics pipelines.**
>
> Philip Ewels, Alexander Peltzer, Sven Fillinger, Harshil Patel, Johannes Alneberg, Andreas Wilm, Maxime Ulysse Garcia, Paolo Di Tommaso & Sven Nahnsen.
>
> _Nat Biotechnol._ 2020 Feb 13. doi: [10.1038/s41587-020-0439-x](https://dx.doi.org/10.1038/s41587-020-0439-x).
