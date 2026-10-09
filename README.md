# Indian Election Data Analysis

Exploratory and statistical analysis of Indian state assembly (Vidhan Sabha) and parliamentary (Lok Sabha) election results using pandas, SciPy, seaborn and matplotlib.

## What it covers

**Vidhan Sabha**
- Data cleaning (party abbreviations, missing constituency names, candidate gender)
- Candidate gender mix, average candidates per seat, voter turnout by year and state
- Top parties, vote share vs seat share
- Gujarat case study: seats won, vote share trends, victory margins

**Lok Sabha**
- Gender representation: candidates, winners and win rate
- Seats won and national vote share of the top parties over time
- Vote concentration: Gini coefficient and Lorenz curve
- Skewness and kurtosis of vote shares (overall, by year, by party)
- One-way ANOVA (a party's vote share across states) and Welch t-test (BJP vs major opposition parties)
- Correlation of party vote shares, incumbency retention rate, vote share swing

## Data

Loaded directly from public CSVs (see the first code cell), so an internet connection is needed:

- `ind-lok-sabha.csv`
- `ind-vidhan-sabha.csv`

## Run it

```bash
pip install -r requirements.txt
jupyter notebook election_analysis.ipynb
```

## Notes

- Winners are the highest-polling candidate in each constituency and election year.
- Incumbency retention compares constituencies by state and seat number; delimitation changes make it an approximation.
- The t-test pools observations across elections, which are not strictly independent, so the p-value is indicative.
