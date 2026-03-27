# Netflix Global Trend Strategy and Content-Analysis
## An End-to-End Data Analytics Case Study (Python + Power BI)

### Project Overview
This project provides a deep-dive analysis of Netflix’s global library to uncover patterns in content acquisition, regional dominance, and production trends. By leveraging a hybrid workflow, I performed complex data engineering in Python to handle unstructured fields and built an executive-level interactive report in Power BI to communicate strategic business insights.

### Tech Stack
**Data Engineering & EDA**: Python (Pandas, NumPy)

**Visualization & Reporting**: Power BI (DAX, Interactive Dashboards)

**Analysis Logic**: Time-Series Analysis, Content Gap Analysis, Multi-label Distribution.

### Phase 1: Data Engineering & Pre-processing (Python)
Using Pandas, I transformed the raw dataset into a clean, analytical schema:

**Missing Value Imputation**: Handled null records to ensure 100% data integrity.

**Multi-label "Explosion(Genre Analysis)**": Since the cast and listed_in (genre) columns contained multiple values per row, I used Python to de-couple and "explode" these strings into individual records for accurate distribution analysis.

**Gap Analysis & Binning**: Engineered a custom "Release Gap" metric by calculating the difference between release_year and date_added. I created Strategic Bins to classify content as:

New Release (Added < 1 year from release)

Recent (Added 2–10 years)

Vintage/Classic (Added > 10 years).

### Phase 2: Deep-Dive Analytics (Python)
I performed specialized Python-driven analyses to answer key business questions:

**Time-Series Analysis**: Tracked the exponential growth of content additions from 2008 to 2021.

**TV Show Longevity**: Analyzed the duration column (seasons) to identify patterns in show cancellation vs. multi-season renewals.

**Movie Runtime Trends**: Aggregated and averaged movie runtimes per year to observe shifting viewer preferences.

**Rating-wise Distribution**: Segmented the library by target audience (TV-MA, PG-13, etc.) to understand demographic focus.

### Phase 3: Visual Intelligence & Reporting (Power BI)

The cleaned data was imported into Power BI to create a Dashboard and 5-page detailed report using the Observation-Insight-Recommendation framework:

**Country Distribution**: Mapped the global footprint, highlighting the US and India as primary growth engines.

**Genre Treemap**: Visualized the dominance of "International Movies" as a key driver for global market expansion.

**Cast Analysis**: Identified "Anchor Stars" who drive massive engagement in regional markets (e.g., Bollywood veteran actors).

### Key Business Findings
**Freshness-First Strategy**: 50% of Netflix’s library consists of New Releases, indicating a heavy reliance on high-frequency content cycles to drive monthly active users (MAU).

**Regional Pivot**: India has emerged as the clear #2 market (972 titles), suggesting a successful strategic shift toward the Asian market to offset Western saturation.

**TV Show Churn**: The longevity analysis reveals that the majority of TV shows do not exceed 1 seasons, supporting a "Limited Series" production model to reduce long-term investment risk.

### Challenges Overcome
**String Manipulation Complexity**: Handling the cast column was difficult due to the high volume of unique names. I used Python’s str.split and explode functions to ensure actors like Anupam Kher or Shah Rukh Khan were accurately counted across all titles.

**Gap Bin Analysis** : Create the Bins by python's function .cut for finding the New Releases , Recent TV shows and Movies, Vintage , Classic and old contents and got the result that netflix focused mostly on **New Releasses** 

**Time-Series Accuracy**: The date_added column had inconsistent formats and nulls. I used Python's to_datetime with error handling to ensure the yearly distribution trends were mathematically sound.

