# Contributing

## Requirements

- [`uv`](https://docs.astral.sh/uv/)
- [`just`](https://github.com/casey/just)

## Setup

Fork this repository and clone your fork:

```console
git clone https://github.com/<your-username>/csan.git
cd csan
```

Sync dependencies:

```console
uv sync --locked
```

Create a branch for your changes:

```console
git switch -c <short-desc>
```

## Commands

### Format/Lint

This project uses [`ruff`](https://docs.astral.sh/ruff/) for formatting and linting. 

Format: 

```console
just format
```

Lint: 

```console
just lint
```

Run both:

```console
just ruff
```

### Tests

```console
just test
```

### Static Typing Checks

```console
just static
```

### All Checks

```console
just check
```

Runs all of the above commands. This is equivalent to what will be run in CI for a specific Python version. 

**Important**: run `just check` before submitting a pull request.


## Commit messages

Use [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/#specification).

## Legal

By contributing, you agree that your contributions will be licensed under the repository license.

