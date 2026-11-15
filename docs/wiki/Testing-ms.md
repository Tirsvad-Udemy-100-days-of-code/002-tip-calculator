# Ujian

🌐 [English](Testing) · [Dansk](Testing-da) · **Bahasa Melayu**

Ujian menggunakan `unittest` daripada pustaka standard Python, jadi tiada
apa-apa tambahan perlu dipasang. Pasang projek dahulu (`pip install -e .`,
lihat [Pemasangan](Install-ms)).

## Jalankan ujian

Dari akar repositori:

```bash
python -m unittest
```

Untuk melihat nama dan keputusan setiap ujian:

```bash
python -m unittest -v tests.test_calculator
```

## Apa yang diuji

`tests/test_calculator.py` menguji `bill_per_person` dalam `calculator.py`:

| Ujian | Menyemak |
| --- | --- |
| `test_course_example` | 124.56 dengan tip 12% untuk 7 orang memberikan 19.93 |
| `test_tip_split_five_ways` | 150 dengan tip 12% untuk 5 orang memberikan 33.6 |
| `test_zero_people_raises` | 0 orang menimbulkan `ValueError` |

Konsol dalam `main.py` tidak dilindungi ujian; ia hanya membaca input dan
mencetak.

## Tambah ujian

Tambah kaedah pada `BillPerPersonTests`. Namanya mesti bermula dengan `test_`:

```python
def test_no_tip(self):
    self.assertEqual(bill_per_person(100, 0, 4), 25.0)
```

Jalankan `python -m unittest` sekali lagi dan semak ia lulus.
