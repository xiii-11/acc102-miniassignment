# acc102-miniassignment
This project analyzes how major Apple events are associated with stock price movements, trading volume, and volatility

# Apple Stock Event Analysis Using WRDS

## 1. Problem & User
This project examines how Apple’s stock price, returns, volume, and volatility behave around major company events such as earnings announcements, product launches, and corporate actions. It is designed for users who want a simple event-based analysis of stock market behavior using Python and WRDS data.

## 2. Data
The data comes from the WRDS CRSP database, accessed through Python using the `wrds` package. The data was retrieved for Apple Inc. (PERMNO 14593) for the period from 2020-01-01 to 2024-12-31. Key fields used in the analysis include `date`, `permno`, `prc`, `ret`, `vol`, and `shrout` from `crsp.dsf`, as well as company identifier information from `crsp.stocknames`.

## 3. Methods
The project was completed in Python using the following main steps:
- Connected to WRDS and downloaded Apple daily stock data from CRSP
- Cleaned the data by converting data types, handling missing values, and correcting price signs
- Created new variables such as market cap proxy, moving averages, rolling volatility, and volume averages
- Built a small event dataset with selected Apple earnings announcements, product launches, and corporate actions
- Mapped event dates to trading days and extracted event windows around each event
- Calculated summary statistics for pre-event and post-event returns, volatility, volume, and price changes
- Visualized stock price trends, return distributions, event windows, and event-type comparisons
- Saved tables and figures into the `outputs/tables` and `outputs/figures` folders

## 4. Key Findings
- Apple’s stock price shows noticeable short-term movement around major events, especially earnings announcements and product launches.
- Trading volume tends to increase around important company events, suggesting stronger investor attention.
- Post-event returns differ across event types, with some events followed by stronger positive average returns than others.
- Rolling volatility changes around event dates, indicating that uncertainty may rise near major announcements.
- Event window plots help show how Apple’s price evolves before and after each selected event.

## 5. How to run
1. Install the required libraries:
   ```bash
   pip install -r requirements.txt
- Make sure you have access to WRDS and valid login credentials.
- Open the Jupyter Notebook or Python script and run all cells.

## 6. Product link / Demo
- GitHub repository link:
  https://github.com/xiii-11/acc102-miniassignment

## 7. Limitations & next steps
This project is based on a small manually selected event list, so the results are mainly descriptive rather than a full formal event study. In the future, the project could be improved by adding more events, including benchmark market returns, and calculating abnormal returns using a more advanced event study method.
