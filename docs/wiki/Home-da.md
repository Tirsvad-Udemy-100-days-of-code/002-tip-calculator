# Drikkepengeberegner

🌐 [English](Home) · **Dansk** · [Bahasa Melayu](Home-ms)

En begyndervenlig konsolapp, der deler en restaurantregning med drikkepenge. Den
er dag 2 af kurset 100 Days of Code. Du skriver regningen, drikkepengeprocenten
og antallet af personer, og den udskriver, hvad hver person skal betale.

| Side | Læs den, når du vil |
| --- | --- |
| [Installation](Install-da) | Sætte Python og projektet op og kontrollere, at det virker |
| [Brug](Usage-da) | Køre beregneren og se en komplet eksempelsession |
| [Sådan virker den](How-It-Works-da) | Forstå formlen og hvordan koden er organiseret |
| [Test](Testing-da) | Køre enhedstestene og tilføje en ny |

## Overblik

| | |
| --- | --- |
| Sprog | Python 3.13 eller nyere |
| Afhængigheder | Ingen (kun standardbiblioteket) |
| Startkommando | `tip-calculator` eller `python -m tip_calculator` |
| Tests | `python -m unittest` |

## Repositoriets opbygning

```
002-tip-calculator/
  src/tip_calculator/
    calculator.py    beregningen, uden input eller output
    main.py          konsollen: stiller spørgsmål, udskriver svaret
    __main__.py      lader dig køre den med python -m tip_calculator
  tests/             enhedstest af beregningen
  docs/wiki/         denne wiki
  framework/         SQA og QC-frameworket (git-submodul)
  pyproject.toml     pakkeoplysninger og kommandoen tip-calculator
```

## Links

- [Repository][repository]
- [Fejlsporing][issues]

[repository]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/002-tip-calculator
[issues]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/002-tip-calculator/issues
