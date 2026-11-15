# Cara Ia Berfungsi

🌐 [English](How-It-Works) · [Dansk](How-It-Works-da) · **Bahasa Melayu**

## Formula

```
tip          = bill × tip_percent / 100
total        = bill + tip
per person   = round(total / people, 2)
```

Contoh pengiraan, yang daripada kursus: bil 124.56, tip 12% dan 7 orang.

| Langkah | Pengiraan | Hasil |
| --- | --- | --- |
| Tip | 124.56 × 0.12 | 14.9472 |
| Jumlah | 124.56 + 14.9472 | 139.5072 |
| Seorang | 139.5072 ÷ 7 = 19.9296, dibundarkan kepada 2 tempat perpuluhan | **19.93** |

Hasil dibundarkan sekali sahaja, di akhir, bukan pada setiap langkah.

## Kod

Pengiraan dan konsol diasingkan, supaya pengiraan boleh diuji tanpa menaip
apa-apa.

| Fail | Tanggungjawab |
| --- | --- |
| `src/tip_calculator/calculator.py` | `bill_per_person(bill, tip_percent, people)` memulangkan jumlah sebagai `float`. Ia tidak mempunyai input atau output |
| `src/tip_calculator/main.py` | `main()` bertanya tiga soalan, memanggil `bill_per_person` dan mencetak jawapan |
| `src/tip_calculator/__main__.py` | Memanggil `main()` supaya `python -m tip_calculator` berfungsi |

Arahan `tip-calculator` diisytiharkan dalam `pyproject.toml` di bawah
`[project.scripts]` dan menuding ke `tip_calculator.main:main`.

## Peraturan dalam `bill_per_person`

- `people` mestilah sekurang-kurangnya 1, jika tidak ia menimbulkan `ValueError("people must be at least 1")`.
- Ia tidak menyemak bil atau peratusan tip; nilai negatif memberikan hasil
  negatif.
- Pembundaran menggunakan `round` Python pada nilai titik terapung binari, jadi
  hasil yang kelihatan seperti nilai tengah tepat (contohnya `x.xx5`) boleh
  dibundarkan ke atas atau ke bawah.
