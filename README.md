# Jaeger-Microservices-MultiLang-AWS-Lambda

## Introduction

Welcome to the Jaeger Microservices repository! This collection of AWS Lambda functions is designed to streamline various aspects of stock trading and AWS Lambda functions are purpose-built to optimize different facets of stock trading and asset management, encompassing functionalities like buying, selling, adding to cart, order history tracking, and home management through the Alpaca API.

With functions written in Python and .NET,and java  Each function is intricately configured with OpenTelemetry to enable comprehensive distributed tracing through Jaeger.

## Functions Included:

### SellStock.py (Python)

Sell a specified quantity of a particular stock using the Alpaca API. This function provides a straightforward and efficient way to manage your stock portfolio.

Dependencies: Alpaca API, Python 3.x, alpaca_trade_api library.

Configuration: Replace API_KEY and API_SECRET with your actual Alpaca API credentials.

Usage: Run the script, input the stock symbol and quantity, and let the function handle the rest.

### AddToCartService.py (Python)

The AddToCartService.py Python Lambda function allows you to add a specific stock to a virtual shopping cart, enabling future reference and management.

Dependencies: This function relies on the Alpaca API for interaction with financial data, requires Python 3.x for execution, and employs the alpaca_trade_api library. Make sure to install this library using pip install alpaca_trade_api.

Configuration: Before utilizing this function, replace the placeholders API_KEY and API_SECRET in the code with your actual Alpaca API credentials.

Usage: To use this service, execute the script. When prompted, input the stock symbol you want to add to the cart (e.g., AAPL). The script will then process the request, adding the specified stock to the cart for future reference in your portfolio management.


### AssetService.cs (.NET)

Retrieve and manage a list of active assets using the Alpaca API. This function introduces random time delays to simulate a more complex function.

Dependencies: AWS Lambda, Alpaca API, OpenTelemetry, Jaeger.

Configuration: Set ALPACA_API_KEY and ALPACA_SECRET_KEY with your Alpaca API credentials.

Usage: Deploy the Lambda function, configure environment variables, and invoke it to retrieve the list of active assets.

### OrderHistoryService.cs (.NET)

Retrieve and display a list of historical orders using the Alpaca API. This function leverages OpenTelemetry for distributed tracing.

Dependencies: AWS Lambda, Alpaca API, OpenTelemetry, Jaeger.

Configuration: Set ALPACA_API_KEY and ALPACA_SECRET_KEY with your Alpaca API credentials.

Usage: Deploy the Lambda function, configure environment variables, and invoke it to retrieve the order history.

### HomeService.java (Java)

Provide an overview of available tradable stocks using the Alpaca API.

Dependencies: Alpaca API, Java Development Kit (JDK), AWS Lambda.

Configuration: Replace placeholders API_KEY and API_SECRET with your actual Alpaca API credentials.

Usage: Deploy the Lambda function, set environment variables, and invoke it to list available tradable stocks.

### BuyService.java (Java)

Enable the purchase of a specified quantity of a chosen stock using the Alpaca API.

Dependencies: Alpaca API, Java Development Kit (JDK), AWS Lambda.

Configuration: Replace placeholders API_KEY and API_SECRET with your actual Alpaca API credentials.

Usage: Deploy the Lambda function, set environment variables, and invoke it to buy stocks.

## Deploy to AWS Lambda

Package each function as per the AWS Lambda documentation.

Ensure you set the environment variables (ALPACA_API_KEY and ALPACA_SECRET_KEY) in AWS Lambda for each function.
Test the functions within the AWS Lambda environment.

## Invoke the Functions

Use AWS Lambda's testing features to invoke each function and ensure they perform as expected.

Remember to handle any additional configurations or permissions that AWS Lambda may require based on your specific use case.










