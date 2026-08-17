# Zillow Housing Market Analysis by Region

Another cleaned-up lab from the same applied Pandas course. this one uses Zillow's historical housing dataset to look at how listing prices, time-on-market, and inventory differ across states, then rolls those states up into broader U.S. regions to compare supply and demand trends.

## What's in this repo

- `zillow-housing-market-analysis.ipynb` — the full analysis
- `README.md` — this file

## What I did

- Converted date strings to proper datetime objects and filtered down to a handful of states to keep the initial line plot readable
- Grouped and aggregated median listing price by date and region, then plotted trends over time in seaborn
- Cleaned missing values out of the days-on-market column and used box plots to compare distributions by state, then found the chart was still cluttered with too many individual states
- Built a new region column with `np.select()`, mapping each state into Northeast, Midwest, South, or West, and re-plotted the box plots at the regional level, which made the pattern much clearer
- Used scatter plots and a faceted `relplot()` to compare days-on-market against housing inventory, split out by region

## The short version

Grouping by region instead of state made the supply and demand story much easier to read. The Midwest looks like it's gaining ground, likely due to affordability, while the Northeast has the highest prices right now but is dealing with tight inventory and high costs, and the West is constrained by high home prices overall. The relationship between days-on-market and inventory also plays out differently by region, not one uniform national pattern.

## Tools

Pandas, numpy, matplotlib, and seaborn.
