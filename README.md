# COVID-19 Visualizer

An interactive **3D globe map** of COVID-19 statistics — click any country to pull live case data scraped from Worldometers.

![Flask](https://img.shields.io/badge/Flask-Python-000000?style=flat-square&logo=flask&logoColor=white)
![amCharts](https://img.shields.io/badge/Globe-amCharts_4-FF6B35?style=flat-square)

## Features

- Rotating **orthographic globe** (amCharts 4)
- Per-country drill-down via `/info/<country_code>`
- Live scraping of Worldometers data with **BeautifulSoup**
- Bootstrap 3 UI shell
- Country code resolution via **pycountry**

## Tech stack

| Layer | Choice |
|-------|--------|
| Backend | Flask |
| Scraping | BeautifulSoup4, requests |
| Globe | amCharts 4 (CDN) |
| Styling | Bootstrap 3 |

## Quick start

```bash
pip install flask beautifulsoup4 requests pycountry
python app.py
```

Open **http://127.0.0.1:5000**

## Project layout

```
app.py
templates/
  visualizer.html   # Globe + country picker
  base.html
static/css.css
```

## Notes

Data source is third-party HTML — scraping may break if the site layout changes. Built as a 2020-era data-viz experiment.

---

[malimba](https://github.com/malimba)
