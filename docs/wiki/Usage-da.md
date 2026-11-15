# Brug

🌐 [English](Usage) · **Dansk** · [Bahasa Melayu](Usage-ms)

## Start appen

Efter [installationen](Install-da) bruger du en af kommandoerne:

```bash
tip-calculator
python -m tip_calculator
```

## De tre spørgsmål

| Spørgsmål | Du skriver | Type |
| --- | --- | --- |
| What was the total bill? | Regningen før drikkepenge, for eksempel `124.56` | Tal, decimaler er tilladt |
| What percentage tip would you like to give? | Et helt tal, for eksempel `12` | Heltal |
| How many people to split the bill? | Et helt antal på mindst `1`, for eksempel `7` | Heltal |

Spørgsmålene stilles på engelsk. Programmet foreslår 10, 12 eller 15, men alle
hele tal accepteres.

## Eksempelsession

```
Welcome to the tip calculator!
What was the total bill? $124.56
What percentage tip would you like to give? 10, 12, or 15? 12
How many people to split the bill? 7
Each person should pay: $19.93
```

## Kendte begrænsninger

Appen kontrollerer ikke, hvad du skriver, før den bruger det. Disse input
afslutter programmet med en Python-fejlmeddelelse i stedet for at spørge igen:

| Input | Resultat |
| --- | --- |
| Tekst, der ikke er et tal, som regning | `ValueError` |
| Et decimaltal som `12.5` som drikkepenge eller antal personer | `ValueError` |
| `0` eller et negativt tal som antal personer | `ValueError: people must be at least 1` |

Kør programmet igen med gyldige værdier.
