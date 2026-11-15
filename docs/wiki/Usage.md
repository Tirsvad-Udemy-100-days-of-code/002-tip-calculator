# Usage

🌐 **English** · [Dansk](Usage-da) · [Bahasa Melayu](Usage-ms)

## Start the app

After [installing](Install), use either command:

```bash
tip-calculator
python -m tip_calculator
```

## The three questions

| Question | You type | Type |
| --- | --- | --- |
| What was the total bill? | The bill before tip, for example `124.56` | Number, decimals allowed |
| What percentage tip would you like to give? | A whole number, for example `12` | Whole number |
| How many people to split the bill? | A whole number of at least `1`, for example `7` | Whole number |

The prompt suggests 10, 12 or 15, but any whole number is accepted.

## Example session

```
Welcome to the tip calculator!
What was the total bill? $124.56
What percentage tip would you like to give? 10, 12, or 15? 12
How many people to split the bill? 7
Each person should pay: $19.93
```

## Known limits

The app does not check what you type before using it. These inputs end the
program with a Python error message instead of asking again:

| Input | Result |
| --- | --- |
| Text that is not a number for the bill | `ValueError` |
| A decimal such as `12.5` for the tip or the people | `ValueError` |
| `0` or a negative number for the people | `ValueError: people must be at least 1` |

Run the program again with valid values.
