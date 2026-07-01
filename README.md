📊 Datasets


Bitcoin Market Sentiment Dataset
Columns: Date, Classification (Fear / Greed / Extreme Fear / Extreme Greed)
Historical Trader Data (Hyperliquid)
Columns include: account, symbol, execution price, size, side, time, start position, event, closedPnL, leverage, etc.



⚙️ Setup

Requirements:

bashpip install pandas numpy matplotlib seaborn scipy

Run the analysis:

bashpython analysis.py

Make sure both CSV files are placed inside a data/ folder next to the script before running.


🔍 Methodology


Data Cleaning — Standardized column names (lowercased), parsed timestamps, coerced numeric fields, removed duplicates and rows with missing critical values.
Merge — Joined trader records to daily sentiment classification on date.
Analysis

Overall profitability and win rate
Average PnL by sentiment (Fear vs Greed), with a statistical significance test (Welch's t-test)
Long vs short performance by sentiment
Leverage usage and its interaction with PnL across sentiment regimes
Most traded coins
Correlation between PnL, leverage, and position size
Account-level performance (to avoid conclusions skewed by a few large accounts)



Outputs — All charts saved to output/, merged dataset exported as CSV, and a plain-text summary of key metrics generated automatically.



📈 Key Findings

(Fill this in after running the script — pull the numbers from output/summary.txt)


Average PnL during Fear: ___
Average PnL during Greed: ___
Statistical significance of the difference: ___ (p-value from t-test)
Leverage usage: higher during ___, correlating with ___
Long/short bias: traders favored ___ positions during ___ sentiment
Most traded asset: ___



💡 Strategy Recommendations

(Derive 3–5 bullet points from the findings above, e.g.)


Reduce position leverage during Extreme Greed periods, where average PnL was ___% lower / more volatile than during Fear.
Consider contrarian positioning during Extreme Fear, where win rate was ___%.
Monitor sentiment-driven crowding in ___, the most heavily traded asset during Greed phases.



🛠️ Tech Stack


Python 3.12
pandas, numpy — data processing
matplotlib, seaborn — visualization
scipy — statistical testing



👤 Author

Deshaveni Akshar Rao
Submitted as part of the Primetrade.ai Data Science hiring assignment.
