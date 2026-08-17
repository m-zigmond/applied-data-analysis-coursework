# Death Records: Demographics, Marital Status, and Age Patterns

This one started as a weekly lab for a semester-long applied Pandas course, and I've cleaned it up here to stand on its own. I'm working with a large U.S. death records dataset alongside its reference tables (race codes, marital status codes) to look for patterns across race, age, and marital status, and to practice turning a messy, code-heavy government dataset into something readable.

## What's in this repo

- `death-records-demographics-analysis.ipynb` — the full analysis
- `README.md` — this file

## What I did

- Loaded the main death records dataset plus two decoder tables (race, marital status) and used them to translate numeric codes into readable labels
- Iteratively cleaned bar charts by removing dominant outlier categories (and a `999` sentinel value used as a missing-age placeholder) so the rest of the distribution became visible instead of getting flattened by a couple of huge bars
- Built box plots in seaborn to compare age distributions across marital status categories
- Filtered and re-plotted marital status breakdowns at three specific ages (60, 70, 80) to see how the distribution shifts over time

## The short version

Once the `999` placeholder and a couple of dominant race categories were removed, the real distribution across smaller demographic groups became visible. Age at death varies meaningfully by marital status. widowed individuals skew older on average than married individuals, with a wider spread of outliers. Looking at 60, 70, and 80 year olds side by side, the marital status mix shifts noticeably older, more widowed, fewer married. as age increases.

## Tools

Pandas, matplotlib, and seaborn.

