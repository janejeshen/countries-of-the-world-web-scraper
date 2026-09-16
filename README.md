# Web Scraping — Week 1 Assignment (Countries of the World)

A **starter** Jupyter notebook for the Cyber Shujaa *Data & AI Specialist Program*,
Week 1 / Assignment 1: **Web Data Scraping** — hands-on practice of the
*Data Understanding* and *Data Preparation* steps of the Data Science Methodology.

## The task

Scrape all **250 countries** from a single live page —
[scrapethissite.com/pages/simple/](https://www.scrapethissite.com/pages/simple/)
("Countries of the World: A Simple Example") — and collect **name, capital,
population, and area** per country.

The page is deliberately **not** built as a `<table>` (unlike the in-class hockey
demo), so the normal four-step pattern must be adapted:

1. **Fetch** the page over HTTP (`requests`)
2. **Parse** the HTML with BeautifulSoup (`html.parser`)
3. **Find the repeating structure** (each country's block + inner tags)
4. **Collect into a pandas DataFrame**

## Pipeline in the notebook (Step 1 → Step 10)

- `Step 1` – import `requests`, `bs4.BeautifulSoup`, `pandas`
- `Step 2` – check the site's `robots.txt` and general policies
- `Step 3` – fetch the page and assert a `2xx` status
- `Step 4` – parse into a BeautifulSoup tree
- `Step 5` – locate every repeating country block
- `Step 6` – extract the four fields from each block
- `Step 7` – build a DataFrame
- `Step 8` – Data Preparation: inspect missing values, duplicates, and fix data types (`population`, `area_km2` come out as text)
- `Step 9` – export to CSV (`assignment1_janenjuguna.csv`)
- `Step 10` – reflection on the hardest part

This is a **scaffold**: cells marked `# TODO` are left for you to complete.

## Run it

Open with Jupyter / VS Code / Colab and run cells top to bottom. The core Python
libraries are pre-installed in Colab; locally you may need:

```bash
pip install requests beautifulsoup4 pandas
```

## Deliverables (as per the assignment brief)

- this notebook (`.ipynb`)
- the exported `.csv` file from Step 9 (e.g. `assignment1_janenjuguna.csv`)

## Layout

```
web_scraping_week1_assignment.ipynb   # the assignment notebook (starter with TODOs)
```