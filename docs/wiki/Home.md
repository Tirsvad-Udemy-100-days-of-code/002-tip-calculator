# Tip Calculator

🌐 **English** · [Dansk](Home-da) · [Bahasa Melayu](Home-ms)

A beginner-friendly console app that splits a restaurant bill with a tip. It is
Day 2 of the 100 Days of Code course. You type the bill, the tip percentage and
the number of people, and it prints what each person pays.

| Page | Read it when you want to |
| --- | --- |
| [Install](Install) | Set up Python and the project, and check that it works |
| [Usage](Usage) | Run the calculator and see a full example session |
| [How It Works](How-It-Works) | Understand the formula and how the code is organised |
| [Testing](Testing) | Run the unit tests and add a new one |

## At a glance

| | |
| --- | --- |
| Language | Python 3.13 or newer |
| Dependencies | None (standard library only) |
| Start command | `tip-calculator` or `python -m tip_calculator` |
| Tests | `python -m unittest` |

## Repository layout

```
002-tip-calculator/
  src/tip_calculator/
    calculator.py    the calculation, no input or output
    main.py          the console: asks questions, prints the answer
    __main__.py      lets you run it with python -m tip_calculator
  tests/             unit tests for the calculation
  docs/wiki/         this wiki
  framework/         the SQA and QC framework (git submodule)
  pyproject.toml     package metadata and the tip-calculator command
```

## Links

- [Repository][repository]
- [Issue tracker][issues]

[repository]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/002-tip-calculator
[issues]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/002-tip-calculator/issues
