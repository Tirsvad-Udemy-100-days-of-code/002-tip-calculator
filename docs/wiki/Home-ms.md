# Kalkulator Tip

🌐 [English](Home) · [Dansk](Home-da) · **Bahasa Melayu**

Aplikasi konsol mesra pemula yang membahagikan bil restoran berserta tip. Ia
ialah Hari 2 kursus 100 Days of Code. Anda menaip jumlah bil, peratusan tip dan
bilangan orang, dan ia mencetak jumlah yang perlu dibayar setiap orang.

| Halaman | Baca apabila anda mahu |
| --- | --- |
| [Pemasangan](Install-ms) | Menyediakan Python dan projek, dan menyemak ia berfungsi |
| [Penggunaan](Usage-ms) | Menjalankan kalkulator dan melihat contoh sesi yang lengkap |
| [Cara Ia Berfungsi](How-It-Works-ms) | Memahami formula dan cara kod disusun |
| [Ujian](Testing-ms) | Menjalankan ujian unit dan menambah ujian baharu |

## Sekilas pandang

| | |
| --- | --- |
| Bahasa | Python 3.13 atau lebih baharu |
| Kebergantungan | Tiada (pustaka standard sahaja) |
| Arahan mula | `tip-calculator` atau `python -m tip_calculator` |
| Ujian | `python -m unittest` |

## Susun atur repositori

```
002-tip-calculator/
  src/tip_calculator/
    calculator.py    pengiraan, tanpa input atau output
    main.py          konsol: bertanya soalan, mencetak jawapan
    __main__.py      membolehkan anda menjalankannya dengan python -m tip_calculator
  tests/             ujian unit untuk pengiraan
  docs/wiki/         wiki ini
  framework/         rangka kerja SQA dan QC (submodul git)
  pyproject.toml     maklumat pakej dan arahan tip-calculator
```

## Pautan

- [Repositori][repository]
- [Penjejak isu][issues]

[repository]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/002-tip-calculator
[issues]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/002-tip-calculator/issues
