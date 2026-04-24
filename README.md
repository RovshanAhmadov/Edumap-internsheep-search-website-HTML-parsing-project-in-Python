# Edumap-internsheep-search-website-HTML-parsing-project-in-Python
Python scraper for Edumap internship/vacancy listings that parses all paginated results and exports a clean table (CSV/XLSX) with posting date, title, and link.
## What it does

- Scrapes `https://edumap.az/vakansiyalar`
- Follows pagination (`?page=2`, `?page=3`, etc.) so results are not limited to page 1
- Deduplicates listings by URL
- Exports one combined dataset

## Tech stack

- Python
- `requests`
- `beautifulsoup4`
- Optional: `pandas`, `openpyxl` for Excel output

## Setup

```bash
python -m pip install requests beautifulsoup4 pandas openpyxl
```

## Run

```bash
python scrape_edumap_vacancies.py --csv "%USERPROFILE%\\Downloads\\edumap_vakansiyalar_all_pages.csv" --xlsx "%USERPROFILE%\\Downloads\\edumap_vakansiyalar_all_pages.xlsx"
```

## Output columns

- `page`
- `published_at`
- `title`
- `url`
