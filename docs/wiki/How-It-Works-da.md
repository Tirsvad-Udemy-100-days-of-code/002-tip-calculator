# Sådan virker den

🌐 [English](How-It-Works) · **Dansk** · [Bahasa Melayu](How-It-Works-ms)

## Formlen

```
tip          = bill × tip_percent / 100
total        = bill + tip
per person   = round(total / people, 2)
```

Gennemregnet eksempel, det fra kurset: en regning på 124,56, 12 % i drikkepenge
og 7 personer.

| Trin | Udregning | Resultat |
| --- | --- | --- |
| Drikkepenge | 124,56 × 0,12 | 14,9472 |
| Total | 124,56 + 14,9472 | 139,5072 |
| Pr. person | 139,5072 ÷ 7 = 19,9296, rundet til 2 decimaler | **19,93** |

Resultatet rundes én gang, til sidst, ikke i hvert trin.

## Koden

Beregningen og konsollen er adskilt, så beregningen kan testes uden at skrive
noget.

| Fil | Ansvar |
| --- | --- |
| `src/tip_calculator/calculator.py` | `bill_per_person(bill, tip_percent, people)` returnerer beløbet som en `float`. Den har hverken input eller output |
| `src/tip_calculator/main.py` | `main()` stiller de tre spørgsmål, kalder `bill_per_person` og udskriver svaret |
| `src/tip_calculator/__main__.py` | Kalder `main()`, så `python -m tip_calculator` virker |

Kommandoen `tip-calculator` er erklæret i `pyproject.toml` under
`[project.scripts]` og peger på `tip_calculator.main:main`.

## Regler i `bill_per_person`

- `people` skal være mindst 1, ellers rejser den `ValueError("people must be at least 1")`.
- Den kontrollerer ikke regningen eller drikkepengeprocenten; en negativ værdi
  giver et negativt resultat.
- Afrunding bruger Pythons `round` på en binær kommatalsværdi, så et resultat,
  der ligner en præcis midte (for eksempel `x.xx5`), kan runde op eller ned.
