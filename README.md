# Trading Behavior Analysis: Fear and Greed Index

## Overview
An exploratory data analysis project that investigates the relationship between market sentiment (Fear and Greed Index) and trading behavior. This analysis examines how different market sentiment classifications affect trader performance, trade characteristics, and profitability.

## Project Structure

```
ds_Jain_Tirth/
│
├── notebook_1.ipynb          # Main Jupyter notebook with complete analysis
├── ds_report.pdf             # Detailed analysis report
├── README.md                 # Project documentation
│
├── csv_files/                # Data directory
│   ├── fear_greed_index.csv  # Fear and Greed Index historical data
│   └── merged_data.csv       # Merged dataset combining trading and sentiment data
│
└── outputs/                  # Visualization outputs
    ├── Avg Closed Pnl by Market Sentiment.png
    ├── Distribution of Crossed by market Sentiment.png
    ├── Distribution of Direction by market Sentiment.png
    ├── Distribution of Side by market sentiment.png
    ├── Distribution of exceution of price by Market Sentiment.png
    └── Size vs PnL.png
```

## Data Sources

### Fear and Greed Index Dataset
- **File**: `csv_files/fear_greed_index.csv`
- **Columns**: timestamp, value, classification, date
- **Classifications**: Extreme Fear, Fear, Neutral, Greed, Extreme Greed
- **Description**: Historical market sentiment data capturing investor emotions and behaviors

### Trading Data
- **File**: Historical trading data (merged into `merged_data.csv`)
- **Metrics**: Trade size, direction, side (BUY/SELL), closed P&L, execution price, and more
- **Description**: Historical trading transactions with detailed trade characteristics

## Analysis Performed

The Jupyter notebook (`notebook_1.ipynb`) performs the following analyses:

1. **Data Import and Preprocessing**
   - Loading historical trading data and Fear & Greed Index
   - Data cleaning and missing value handling
   - Timestamp conversion to datetime format

2. **Data Merging**
   - Combining trading data with sentiment classifications
   - Aligning timestamps for accurate correlation

3. **Univariate Analysis**
   - Statistical summary of individual variables
   - Distribution analysis of key metrics

4. **Trader Performance by Sentiment**
   - Average Closed P&L across different sentiment classifications
   - Win rate analysis by market sentiment
   - Trade size patterns across sentiment categories

5. **Pattern Identification**
   - Trading behavior patterns under different market conditions
   - Direction analysis (Open Long, Close Short, Open Short, Close Long)
   - Side distribution (BUY vs SELL) by sentiment
   - Crossed trade frequency analysis

6. **Visualizations**
   - Average Closed P&L by Market Sentiment
   - Distribution of trade sides across sentiment classifications
   - Distribution of trade directions by sentiment
   - Execution price distributions
   - Trade size vs P&L scatter plots
   - Crossed trade patterns

## Key Findings

### Profitability by Sentiment
- **Extreme Greed**: Highest average Closed P&L ($67.89) with the best win rate (53.31%)
- **Fear**: Second highest average Closed P&L ($54.29)
- **Greed**: Average Closed P&L of $42.74
- **Extreme Fear & Neutral**: Lowest performance ($34.54 and $34.31 respectively)

### Trading Patterns
- **Side Distribution**: 
  - Tendency towards SELL trades during "Extreme Greed" and "Greed" periods
  - Tendency towards BUY trades during "Extreme Fear" and "Neutral" periods

- **Direction Patterns**:
  - "Open Long" and "Close Short" are most prevalent across all sentiments
  - "Extreme Greed" and "Greed" show higher proportions of "Open Short" and "Close Long" trades

- **Trade Size Insights**:
  - "Fear" sentiment: Highest average winning trade size ($16,238.25) and losing trade size ($17,329.44)
  - "Extreme Greed": Lowest average winning trade size ($5,558.95)
  - No strong linear correlation between trade size and P&L

### Market Behavior
- Crossed trades are frequent across all sentiment classifications
- "Extreme Greed" and "Neutral" show the highest percentages of crossed trades
- Market sentiment provides valuable signals for trading strategy optimization

## How to Run

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Running the Analysis
1. Clone the repository:
```bash
git clone https://github.com/Jain-Tirth/ds_Jain_Tirth.git
cd ds_Jain_Tirth
```

2. Launch Jupyter Notebook:
```bash
jupyter notebook notebook_1.ipynb
```

3. Run all cells sequentially or use "Run All" from the Cell menu

### Google Colab
Click the "Open in Colab" badge at the top of `notebook_1.ipynb` to run the analysis directly in Google Colab.

## Technologies Used
- **Python 3.x**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical data visualization
- **Jupyter Notebook**: Interactive development environment

## Insights for Trading Strategy

Based on the analysis, traders can:
1. **Optimize entry/exit timing** based on sentiment indicators
2. **Adjust position sizing** according to prevailing market sentiment
3. **Leverage sentiment extremes** (especially "Extreme Greed") for higher win rates
4. **Exercise caution** during "Extreme Fear" and "Neutral" periods
5. **Align trading direction** with sentiment-driven market tendencies

## Author
Tirth Jain

## License
This project is available for educational and research purposes.
