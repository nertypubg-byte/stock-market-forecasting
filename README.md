# stock-market-forecasting
Stock market forecasting by kotsov with stock visualization, charts, indicators, and a 7-day forecast

About the project: Stockvision by kotsovvv is a web app for tracking and forecasting stocks. It displays 30-day price history, creates a 7-day forecast, and generates buy/sell/hold signals based on technical indicators.

Russian stock prices are current as of April 2026. (Source: T-investments/Moscow Exchange.) I used stocks I already had in my portfolio.

Features:
30-day price history chart (canvas)
7-day forecast
RSI indicators - overbought/oversold
Volatility indicators
BYU/SELL/HOLD signal
Automatic data update every 30 seconds
Live clock in the header
Support for ruble and dollar stocks

stack:
React 18 - UI
Vite 5 - builder
Canvas API - chart rendering (no third-party libraries)
IBM Plex Mono/Sans - fonts (Google fonts)

How the forecast works:
1) A 30-day price history is generated based on the price + random changes +/- 3%
2) The trend is calculated as the average change over the last 7 days
3) The forecast is constructed as: price + trend + some noise
4) RSI is calculated using a standard formula based on history
5) Signal: RSI < 35 + positive forecast -> BUY, RSI > 65 + negative forecast -> SELL, otherwise HOLD

Disclaimer: Data and forecasts are randomly generated for educational purposes. This does not constitute financial advice. Do not use for real investments.
