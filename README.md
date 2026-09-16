# Countries of the World — Web Scraper

A Jupyter notebook that scrapes all 250 countries of the world from a live web
page and produces a clean CSV — a hands-on exercise in the *Data Understanding*
and *Data Preparation* steps of the Data Science Methodology, from the Cyber
Shujaa *Data & AI Specialist Program* (Week 1: Web Data Scraping).

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

The `# TODO` markers left in comments are from the original starter scaffold —
the code underneath each one is filled in and every step runs end-to-end
(250 rows extracted, cleaned, and exported to CSV).

## Run it

Open with Jupyter / VS Code / Colab and run the cells top to bottom. The core
libraries are pre-installed in Colab; locally you may need:

```bash
pip install requests beautifulsoup4 pandas
```

## Output

- the completed notebook (`.ipynb`)
- the exported CSV from Step 9 (`assignment1_janenjuguna.csv`)

## Layout

```
countries_of_the_world_web_scraper.ipynb   # the completed web-scraping notebook
```