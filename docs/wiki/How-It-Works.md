# How It Works

🌐 **English** · [Dansk](How-It-Works-da) · [Bahasa Melayu](How-It-Works-ms)

## The formula

```
tip          = bill × tip_percent / 100
total        = bill + tip
per person   = round(total / people, 2)
```

Worked example, the one from the course: a bill of 124.56, a 12% tip, 7 people.

| Step | Calculation | Result |
| --- | --- | --- |
| Tip | 124.56 × 0.12 | 14.9472 |
| Total | 124.56 + 14.9472 | 139.5072 |
| Per person | 139.5072 ÷ 7 = 19.9296, rounded to 2 decimals | **19.93** |

The result is rounded once, at the end, not at each step.

## The code

The calculation and the console are separate, so the calculation can be tested
without typing anything.

| File | Responsibility |
| --- | --- |
| `src/tip_calculator/calculator.py` | `bill_per_person(bill, tip_percent, people)` returns the amount as a `float`. It does no input or output |
| `src/tip_calculator/main.py` | `main()` asks the three questions, calls `bill_per_person` and prints the answer |
| `src/tip_calculator/__main__.py` | Calls `main()` so `python -m tip_calculator` works |

The `tip-calculator` command is declared in `pyproject.toml` under
`[project.scripts]` and points to `tip_calculator.main:main`.

## Rules in `bill_per_person`

- `people` must be at least 1, otherwise it raises `ValueError("people must be at least 1")`.
- It does not check the bill or the tip percentage; a negative value gives a
  negative result.
- Rounding uses Python's `round` on a binary floating-point value, so a result
  that looks like an exact tie (for example `x.xx5`) can round up or down.
