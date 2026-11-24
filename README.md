# Global Tech Salaries

A small Python project that generates a synthetic salary dataset for tech jobs across countries and visualizes it with pandas + matplotlib.

## How It Works (English summary)

1. **`scraper.py`** — generates salary records for `Software Developer`, `Cybersecurity Engineer` and `Data Analyst` across `USA`, `Germany`, `India`, `Iran` and `Japan`, using per-country base salaries and per-job multipliers, then saves the dataset to `data/salaries.csv`
2. **`annalysis.py`** — loads `data/salaries.csv`, builds a pivot table of average salary per country/job, and renders a grouped bar chart to `plots/salary_comparison.png`

> **Note:** the dataset is **synthetic** (generated from base-salary tables, not scraped from a live source) — see the `Source: Generated` column in the output.

## Run

```bash
pip install pandas numpy matplotlib
python scraper.py
python annalysis.py
```

## Output

- `data/salaries.csv` — generated dataset (Job, Country, Avg / Min / Max salary in USD)
- `plots/salary_comparison.png` — salary comparison chart

Sample outputs are committed in the repository root (`salaries.csv`, `salary_comparison.png`).

---

## معرفی پروژه

این پروژه شامل دو بخش اصلی است:

- تولید داده‌های نمونه حقوق برای مشاغل مختلف در کشورهای مختلف
- تحلیل و مصورسازی داده‌های تولید شده

## نیازمندی‌ها

- Python 3.8+
- کتابخانه‌های مورد نیاز: pandas، numpy، matplotlib

## نحوه اجرا

```bash
pip install pandas numpy matplotlib
python scraper.py      # تولید داده‌ها
python annalysis.py    # تحلیل و مصورسازی
```

## محدودیت‌ها

۱. عدم احتساب هزینه زندگی در کشورها
۲. نوسانات نرخ ارز در محاسبات
۳. تفاوت‌های منطقه‌ای در هر کشور
