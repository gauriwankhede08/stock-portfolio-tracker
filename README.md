# stock-portfolio-tracker
# portfolio_tracker.py

# ================================
# Simple Stock Portfolio Tracker
# ================================

# Manually defined stock prices and portfolio

# Define your portfolio
portfolio = [
    {'ticker': 'AAPL', 'shares': 10},
    {'ticker': 'MSFT', 'shares': 5},
    {'ticker': 'GOOGL', 'shares': 2},
    {'ticker': 'TSLA', 'shares': 8}
]

# Manually defined stock prices
stock_prices = {
    'AAPL': 195.00,
    'MSFT': 415.50,
    'GOOGL': 2900.00,
    'TSLA': 250.00
}

# Calculate and display total investment
def calculate_total_investment(portfolio, prices):
    total = 0
    print("Your Stock Portfolio:")
    print("-------------------------------")
    for stock in portfolio:
        ticker = stock['ticker']
        shares = stock['shares']
        price = prices.get(ticker, 0)
        value = shares * price
        total += value
        print(f"{ticker}: {shares} shares x ${price:.2f} = ${value:.2f}")
    print("-------------------------------")
    print(f"Total Investment: ${total:.2f}")

# Run the tracker
if __name__ == "__main__":
    calculate_total_investment(portfolio, stock_prices)
