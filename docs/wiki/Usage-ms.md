# Penggunaan

🌐 [English](Usage) · [Dansk](Usage-da) · **Bahasa Melayu**

## Mulakan aplikasi

Selepas [pemasangan](Install-ms), gunakan salah satu arahan:

```bash
tip-calculator
python -m tip_calculator
```

## Tiga soalan

| Soalan | Anda taip | Jenis |
| --- | --- | --- |
| What was the total bill? | Bil sebelum tip, contohnya `124.56` | Nombor, perpuluhan dibenarkan |
| What percentage tip would you like to give? | Nombor bulat, contohnya `12` | Nombor bulat |
| How many people to split the bill? | Nombor bulat sekurang-kurangnya `1`, contohnya `7` | Nombor bulat |

Soalan dipaparkan dalam bahasa Inggeris. Aplikasi mencadangkan 10, 12 atau 15,
tetapi sebarang nombor bulat diterima.

## Contoh sesi

```
Welcome to the tip calculator!
What was the total bill? $124.56
What percentage tip would you like to give? 10, 12, or 15? 12
How many people to split the bill? 7
Each person should pay: $19.93
```

## Had yang diketahui

Aplikasi tidak menyemak apa yang anda taip sebelum menggunakannya. Input
berikut menamatkan program dengan mesej ralat Python dan bukannya bertanya
semula:

| Input | Hasil |
| --- | --- |
| Teks yang bukan nombor sebagai bil | `ValueError` |
| Perpuluhan seperti `12.5` sebagai tip atau bilangan orang | `ValueError` |
| `0` atau nombor negatif sebagai bilangan orang | `ValueError: people must be at least 1` |

Jalankan program sekali lagi dengan nilai yang sah.
