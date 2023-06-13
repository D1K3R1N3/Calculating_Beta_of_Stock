# Calculating_Beta_of_Stock
This code calculates the beta value of a given stock (THYAO.IS) with respect to the market (XU100.IS). Beta is a measure of a stock's sensitivity to market movements.

## Prerequisites
Python 3.x
Required Libraries: numpy, pandas, pandas_datareader
## Installation
Install Python: Visit the official Python website (https://www.python.org) and download the latest version of Python for your operating system.
Install required libraries by running the following command in your terminal or command prompt:
pip install numpy pandas pandas_datareader
## Usage
Open your preferred Python IDE or text editor.
Copy and paste the provided code into a new Python file (e.g., beta_calculation.py).
Run the code.
## Description
The code imports necessary libraries: numpy, pandas, pandas_datareader, and datetime.
It defines a stock ticker symbol t as "THYAO.IS" and creates a list of tickers containing the stock symbol and the market symbol ('XU100.IS').
An empty DataFrame data is created to store the retrieved stock data.
A loop iterates through the tickers list and fetches the adjusted close prices of each ticker from Yahoo Finance using the wb.DataReader() function. The data is collected from the start date of '2020-1-1' to the current date.
The logarithmic returns of the stock data are calculated and stored in the sec_returns DataFrame.
The covariance matrix is computed using the cov() function on sec_returns multiplied by 250 (number of trading days in a year).
The covariance of the stock (THYAO.IS) with the market (XU100.IS) is extracted from the covariance matrix.
The variance of the market returns is calculated using the var() function on sec_returns['XU100.IS'] multiplied by 250.
Finally, the beta value is computed as the ratio of the covariance of the stock with the market to the market variance.
## Output
The code provides the following outputs:

The covariance matrix (cov) showing the covariance values between THYAO.IS and XU100.IS.
The covariance of THYAO.IS with XU100.IS (cov_with_market).
The variance of the market returns (market_var).
The beta value of THYAO.IS with respect to XU100.IS (beta).
Please note that the provided values in the code example are for illustrative purposes and may not reflect the actual data.

Feel free to customize the code to suit your specific needs.

## Disclaimer
This code is provided for educational and informational purposes only. It does not constitute financial or investment advice. Use it at your own risk. You should consult with a qualified financial advisor or professional before making any investment decisions. The code may not be accurate, complete, or up-to-date. The author assumes no liability for any errors or omissions in the code or its use.
