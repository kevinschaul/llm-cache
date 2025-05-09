# llm-cache

[![PyPI](https://img.shields.io/pypi/v/llm-cache-plugin.svg)](https://pypi.org/project/llm-cache-plugin/)
[![Changelog](https://img.shields.io/github/v/release/kevinschaul/llm-cache-plugin?include_prereleases&label=changelog)](https://github.com/kevinschaul/llm-cache-plugin/releases)
[![Tests](https://github.com/kevinschaul/llm-cache-plugin/actions/workflows/test.yml/badge.svg)](https://github.com/kevinschaul/llm-cache-plugin/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/kevinschaul/llm-cache-plugin/blob/main/LICENSE)

Check whether you've already run this prompt before calling the LLM

## Installation

Install this plugin in the same environment as [LLM](https://llm.datasette.io/).

```bash
llm install llm-cache-plugin
```

## Usage

This plugin add a `--cache` flag to `llm prompt`.

If `--cache` is specified, the plugin will search your llm database for a previously-saved response for this prompt-system-model combination. If it is found, it returns that text, saving you time and money. If not, it passes off to the regular `llm prompt` command.

```bash
llm 'How many rs are in strawberry? Think very hard.'
> There are 2 'R's in strawberry
```

Took 3.01s user 1.45s system 104% cpu 4.280 total

```bash
llm --cache 'How many rs are in strawberry? Think very hard.'
> There are 2 'R's in strawberry
```

Took 2.83s user 1.50s system 152% cpu 2.836 total

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
