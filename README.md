# ⚡️ Lightning Research Poster Template 🔬

[![Lightning](https://img.shields.io/badge/-Lightning-792ee5?logo=pytorchlightning&logoColor=white)](https://lightning.ai)
![license](https://img.shields.io/badge/License-Apache%202.0-blue.svg)
[![CI testing](https://github.com/Lightning-Universe/Research-poster/actions/workflows/ci-testing.yml/badge.svg?event=push)](https://github.com/Lightning-Universe/Research-poster/actions/workflows/ci-testing.yml)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/Lightning-Universe/Research-poster/main.svg)](https://results.pre-commit.ci/latest/github/Lightning-Universe/Research-poster/main)

Use this app to share your research paper results. This app lets you connect a blogpost, arxiv paper, and a jupyter
notebook and even have an interactive demo for people to play with the model. This app also allows industry
practitioners to reproduce your work.

## Getting started

To create a Research Poster you can install this app via the [Lightning CLI](https://lightning.ai/lightning-docs/) or
[use the template](https://docs.github.com/en/articles/creating-a-repository-from-a-template) from GitHub and
manually install the app as mentioned below.

> ![image](./assets/demo.png)

You can modify the content of this app and customize it to your research.
At the root of this template, you will find [app.py](./app.py) that contains the `ResearchApp` class. This class
provides arguments like a link to a paper, a blog, and whether to launch a Gradio demo. You can read more about what
each of the arguments does in the docstrings.

### 1. Poster Component

This component lets you make research posters using markdown files. The component comes with a predefined poster.md file
in the resources folder that contains markdown content for building the poster. You can directly update the existing
file with your research content.

### 2. Link to Paper, blog and Training Logs

You can add your research paper, a blog post, and training logs to your app. These are usually static web links that can
be directly passed as optional arguments within app.py

### 3. A view only Jupyter Notebook

You can provide the path to your notebook and it will be converted into static HTML.

### 4. Model Demo

To create an interactive demo you’d need to implement the `build_model` and `predict` methods of the ModelDemo class
present
in the `research_app/demo/model.py` module.

### 5. JupyterLab Component

This component runs and adds a JupyterLab instance to your app. You can provide a way to edit and run your code for
quick audience demonstrations. However, note that sharing a JupyterLab instance can expose the cloud instance to
security vulnerability.
