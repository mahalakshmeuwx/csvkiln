# csvkiln

Reusable ETL skeleton for the CSVs I get at work

Built for my own use; public in case it helps someone.

## Features

- Drops duplicates, trims strings, normalizes dates
- Config-driven column renames and type casts
- Writes a cleaning report next to the output
- Chunked reading for files that do not fit in memory

## Install

```bash
pip install -r requirements.txt
```

## Usage

```bash
python pipeline.py raw.csv --config config.yaml --out clean.csv
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── pull_request_template.md
├── docs/
│   ├── configuration.md
│   ├── development.md
│   └── usage.md
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── config.yaml
├── pipeline.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT. Do whatever you want.
