# github-actions-article

A tiny Python example project used to demonstrate a GitHub Actions CI workflow.

If this script was useful to you, consider donating to support the Developer Service Blog: https://buy.stripe.com/bIYdTrggi5lZamkdQW

## What’s in here

- **`calculator.py`**: a minimal `add(a, b)` function.
- **`test_calculator.py`**: a `pytest` unit test for `add`.
- **`.github/workflows/ci.yml`**: CI that runs on pushes/PRs to `main` and executes:
  - `ruff check .`
  - `mypy .`
  - `pytest`
  across Python **3.10**, **3.11**, and **3.12**.

## Requirements

- Python 3.10+

## Setup

```bash
python -m venv .venv
```

Activate the virtual environment:

- **Windows (PowerShell)**:

```powershell
.\.venv\Scripts\Activate.ps1
```

- **macOS/Linux (bash/zsh)**:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run locally

Run tests:

```bash
pytest
```

Run lint:

```bash
ruff check .
```

Run type-checking:

```bash
mypy .
```
