# Test

🌐 [English](Testing) · **Dansk** · [Bahasa Melayu](Testing-ms)

Testene bruger `unittest` fra Pythons standardbibliotek, så der skal ikke
installeres noget ekstra. Installér projektet først (`pip install -e .`, se
[Installation](Install-da)).

## Kør testene

Fra repositoriets rod:

```bash
python -m unittest
```

For at se hver tests navn og resultat:

```bash
python -m unittest -v tests.test_calculator
```

## Hvad testes

`tests/test_calculator.py` tester `bill_per_person` i `calculator.py`:

| Test | Kontrollerer |
| --- | --- |
| `test_course_example` | 124,56 med 12 % i drikkepenge til 7 personer giver 19,93 |
| `test_tip_split_five_ways` | 150 med 12 % i drikkepenge til 5 personer giver 33,6 |
| `test_zero_people_raises` | 0 personer rejser `ValueError` |

Konsollen i `main.py` er ikke dækket af en test; den læser kun input og
udskriver.

## Tilføj en test

Tilføj en metode til `BillPerPersonTests`. Navnet skal begynde med `test_`:

```python
def test_no_tip(self):
    self.assertEqual(bill_per_person(100, 0, 4), 25.0)
```

Kør `python -m unittest` igen og kontrollér, at den består.
