# Pemasangan

🌐 [English](Install) · [Dansk](Install-da) · **Bahasa Melayu**

Kalkulator ini tidak mempunyai kebergantungan pihak ketiga. Anda hanya perlukan
Python dan projek itu sendiri.

## 1. Keperluan

| Keperluan | Sebab |
| --- | --- |
| Python 3.13 atau lebih baharu | `pyproject.toml` menetapkan `requires-python = ">=3.13"` |
| `git` | Untuk mengklon repositori |
| Akses SSH ke `git.tirsystem.com` (port 10022) | Repositori dan submodul `framework/`nya diklon melalui SSH |

## 2. Dapatkan kod

```bash
git clone --recurse-submodules ssh://git@git.tirsystem.com:10022/Tirsvad-Udemy-100-days-of-code/002-tip-calculator.git
cd 002-tip-calculator
```

Jika anda mengklon tanpa `--recurse-submodules`, dapatkan rangka kerja
kemudian:

```bash
git submodule update --init --recursive
```

Kalkulator itu sendiri tidak memerlukan `framework/`; ia hanya penting jika
anda mengusahakan dokumen projek.

## 3. Cipta persekitaran maya dan pasang

```bash
python -m venv .venv
```

Aktifkannya:

```bash
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Linux, macOS, Git Bash
source .venv/bin/activate
```

Kemudian pasang projek dalam mod boleh-edit, supaya arahan `tip-calculator`
dan ujian dapat menemui pakej `tip_calculator` dalam `src/`:

```bash
pip install -e .
```

## 4. Semak ia berfungsi

```bash
python -m unittest
```

Anda patut melihat `OK`. Kemudian teruskan ke [Penggunaan](Usage-ms).
