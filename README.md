# llm-cache

[![PyPI](https://img.shields.io/pypi/v/llm-cache.svg)](https://pypi.org/project/llm-cache/)
[![Changelog](https://img.shields.io/github/v/release/kevinschaul/llm-cache?include_prereleases&label=changelog)](https://github.com/kevinschaul/llm-cache/releases)
[![Tests](https://github.com/kevinschaul/llm-cache/actions/workflows/test.yml/badge.svg)](https://github.com/kevinschaul/llm-cache/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/kevinschaul/llm-cache/blob/main/LICENSE)

Check whether you've already run this prompt before calling the LLM

## Installation

Install this plugin in the same environment as [LLM](https://llm.datasette.io/).
```bash
llm install llm-cache
```
## Usage

Usage instructions go here.

## Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:
```bash
cd llm-cache
python -m venv venv
source venv/bin/activate
```
Now install the dependencies and test dependencies:
```bash
llm install -e '.[test]'
```
To run the tests:
```bash
pytest
```
