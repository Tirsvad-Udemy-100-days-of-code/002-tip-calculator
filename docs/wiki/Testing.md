# Testing

🌐 **English** · [Dansk](Testing-da) · [Bahasa Melayu](Testing-ms)

The tests use `unittest` from the Python standard library, so nothing extra
needs to be installed. Install the project first (`pip install -e .`, see
[Install](Install)).

## Run the tests

From the repository root:

```bash
python -m unittest
```

To see each test's name and result:

```bash
python -m unittest -v tests.test_calculator
```

## What is tested

`tests/test_calculator.py` tests `bill_per_person` in `calculator.py`:

| Test | Checks |
| --- | --- |
| `test_course_example` | 124.56 with a 12% tip for 7 people gives 19.93 |
| `test_tip_split_five_ways` | 150 with a 12% tip for 5 people gives 33.6 |
| `test_zero_people_raises` | 0 people raises `ValueError` |

The console in `main.py` is not covered by a test; it only reads input and
prints.

## Add a test

Add a method to `BillPerPersonTests`. The name must start with `test_`:

```python
def test_no_tip(self):
    self.assertEqual(bill_per_person(100, 0, 4), 25.0)
```

Run `python -m unittest` again and check that it passes.
