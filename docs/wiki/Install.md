# Install

🌐 **English** · [Dansk](Install-da) · [Bahasa Melayu](Install-ms)

The calculator has no third-party dependencies. You only need Python and the
project itself.

## 1. Requirements

| Need | Why |
| --- | --- |
| Python 3.13 or newer | `pyproject.toml` sets `requires-python = ">=3.13"` |
| `git` | To clone the repository |
| SSH access to `git.tirsystem.com` (port 10022) | The repository and its `framework/` submodule are cloned over SSH |

## 2. Get the code

```bash
git clone --recurse-submodules ssh://git@git.tirsystem.com:10022/Tirsvad-Udemy-100-days-of-code/002-tip-calculator.git
cd 002-tip-calculator
```

If you cloned without `--recurse-submodules`, fetch the framework afterwards:

```bash
git submodule update --init --recursive
```

The calculator itself does not need `framework/`; it only matters if you work
on the project's documents.

## 3. Create a virtual environment and install

```bash
python -m venv .venv
```

Activate it:

```bash
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Linux, macOS, Git Bash
source .venv/bin/activate
```

Then install the project in editable mode, so the `tip-calculator` command and
the tests can find the `tip_calculator` package in `src/`:

```bash
pip install -e .
```

## 4. Check that it works

```bash
python -m unittest
```

You should see `OK`. Then continue to [Usage](Usage).
