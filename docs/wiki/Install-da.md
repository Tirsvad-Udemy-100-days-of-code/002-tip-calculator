# Installation

🌐 [English](Install) · **Dansk** · [Bahasa Melayu](Install-ms)

Beregneren har ingen tredjepartsafhængigheder. Du skal kun bruge Python og selve
projektet.

## 1. Forudsætninger

| Behov | Hvorfor |
| --- | --- |
| Python 3.13 eller nyere | `pyproject.toml` sætter `requires-python = ">=3.13"` |
| `git` | Til at klone repositoryet |
| SSH-adgang til `git.tirsystem.com` (port 10022) | Repositoryet og dets `framework/`-submodul klones over SSH |

## 2. Hent koden

```bash
git clone --recurse-submodules ssh://git@git.tirsystem.com:10022/Tirsvad-Udemy-100-days-of-code/002-tip-calculator.git
cd 002-tip-calculator
```

Hvis du klonede uden `--recurse-submodules`, hent frameworket bagefter:

```bash
git submodule update --init --recursive
```

Selve beregneren behøver ikke `framework/`; det har kun betydning, hvis du
arbejder på projektets dokumenter.

## 3. Opret et virtuelt miljø og installér

```bash
python -m venv .venv
```

Aktivér det:

```bash
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Linux, macOS, Git Bash
source .venv/bin/activate
```

Installér derefter projektet i redigerbar tilstand, så kommandoen
`tip-calculator` og testene kan finde pakken `tip_calculator` i `src/`:

```bash
pip install -e .
```

## 4. Kontrollér, at det virker

```bash
python -m unittest
```

Du skal se `OK`. Fortsæt derefter til [Brug](Usage-da).
