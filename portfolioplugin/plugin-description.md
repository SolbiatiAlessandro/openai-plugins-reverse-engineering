The PortfolioPilot plugin is designed to provide a range of services related to investment portfolio management and financial market information. Here's a detailed breakdown of each type definition and their respective fields:

1. `getSecurityDetails`: This type is used to fetch up-to-date information about a specific security. The only field required is `ticker`, which represents the ticker symbol of the security.

2. `getTopETFs`: This type is used to fetch the top 20 Exchange Traded Funds (ETFs) based on certain filters. The fields include:
   - `philosophy`: This can be "Actively Managed", "Passively Managed", or "Strategic Beta".
   - `is_diversified`: This is a boolean field indicating whether the ETFs should be sufficiently diversified.
   - `max_expense_ratio`: This represents the maximum expense ratio for the ETFs.
   - `asset_class`: This can be one of many options like "US Large Cap Equities", "US Mid Cap Equities", "US Small Cap Equities", etc.
   - `listed_country`: This can be "US" or "CA", indicating the country in which the ETF is listed.

3. `getTopStocks`: This type is used to fetch the top 20 stocks with the highest expected Sharpe ratio based on certain filters. The fields include:
   - `sector`: This can be one of many options like "Healthcare", "Energy", "Technology", etc.
   - `min_marketcap`: This represents the minimum market capitalization for the stocks.
   - `country`: This can be "US" or "CA", indicating the country of the stocks.

4. `getPortfolioDetails`: This type is used to get all performance details for a given portfolio. The only field is `portfolio`, which is an array of portfolio items.

5. `getPortfolioExposures`: This type is used to get sector, country, and holding exposures for a given portfolio. The only field is `portfolio`, which is an array of portfolio items.

6. `getAiAssessment`: This type is used to get a portfolio assessment with summary, expected performance, recommendations, and downside protection. The only field is `portfolio`, which is an array of portfolio items.

7. `getMacroInsights`: This type is used to get macro insights of the global economy or a specific region. The only field is `region`, which can be "US", "Canada", or "World".

8. `get_portfolio_item_cumulative_returns`: This type is used to get recent historical returns of all individual items in your portfolio. The fields include:
   - `time_period`: This represents the time period to get the cumulative returns for last 7 to 30 days.
   - `portfolio`: This is an array of portfolio items, each with a `ticker` and `amount`.

In the `portfolio` field for several types, specific tickers are used for non-security assets: `CUR:USD` for cash, `Reserved.RealEstate` for real estate, `Reserved.Crypto` for cryptocurrencies, and `Reserved.MoneyMarket` for money market funds.
