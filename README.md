# VBA Project - Portfolio Optimization

![formula](Images/téléchargé.png)

Team : Ilyès BOUSSOUF; Jardiel Junior DA SILVA ARAUJO; Ikram OUDRA; Ilyasse BENOUNI; Ilyas MASMOUDI

## Objectives


The main objective of this project is to construct an Automated Portfolio Optimization Program in which the user can:
  1. Choose the number of stocks in the portfolio he wants to build.
  2. Import automatically the historical data for each stock with a given ticker (from Yahoo Finance, accessed using alphavantage) to update the data in real-time.
  3. Compute automatically different metrics related to stock performance (returns, volatility, Sharpe Ratio…) and construct the efficient frontier.
  4. The code will optimize the portfolio weights to maximize the Sharpe ratio, optimizing the trade-off between returns and volatility.
  5. Finally, the user can select the “optimal” portfolio and its relative weights.


![formula](Images/portfolio_opt.png)

## Model test

## Test 1

### Inputs

Risk-free Rate : 0.3% \
Number of iterations : 5000

Start Date : 17/01/2000\
End Date : 17/10/2020

Stocks tickers selected :
* AI.PA (Air Liquide)
* AAPL (Apple)
* MSFT (Microsoft)
* NVDA (Nvidia)
* AMZN (Amazon)
* V (Visa)
* MA (Mastercard)
* WMT (Walmart)

Number of Stocks : 8

### Outputs

#### Optimal weights

* AI.PA weight : 3.78%
* AAPL weight : 19.75%
* MSFT weight : 3.18%
* NVDA weight : 8.62%
* AMZN weight : 16.69%
* V weight : 20.06%
* MA weight : 12.67%
* WMT weight : 15.25%

Sump Check = 100%

![formula](Images/optweights.JPG)

#### Optimal portfolio Performance

* Sharpe Ratio : 0.43190822
* Portfolio Average Returns : 2.335%
* Portfolio Standard Deviation : 4.712%

#### Optimization simulations, Optimal Portfolio & Capital Market Line

![formula](Images/portfolio_opt.png)

## Test 2

### Inputs

Risk-free Rate : 0.005 (=0.5%) \
Number of iterations : 10000

Start Date : 10/03/2002\
End Date : 17/05/2021

Stocks tickers selected :
* SAN.PA (Sanofi)
* CAP.PA (Capgemini)
* SGO.PA (Société Générale)
* DIS (The Walt Disney Company)
* BAC (Bank of America Corp)
* WMT (Walmart)
* TSM (Taiwan Semiconductor Manufacturing Company)
* JNJ (Johnson & Johnson)
* MC.PA (LVMH Moët Hennessy)
* ACN (Accenture)

Number of Stocks : 10

### Outputs

#### Optimal weights

* SAN.PA weight : 0.89%
* CAP.PA weight : 6.03%
* SGO.PA weight : 0.16%
* DIS weight : 0.95%
* BAC weight : 13.37%
* WMT weight : 11.71%
* TSM weight : 23.79%
* JNJ weight : 5.32%
* MC.PA weight : 26.07%
* ACN weight : 11.71%

Sump Check = 100%

![formula](Images/weights2.JPG)

#### Optimal portfolio Performance

* Sharpe Ratio : 0.3181
* Portfolio Average Returns : 1.841%
* Portfolio Standard Deviation : 4.214%

![formula](Images/param2.JPG)


#### Optimization simulations, Optimal Portfolio & Capital Market Line

![formula](Images/graph2.JPG)

## Code explanations

We segmented our VBA codes in 3 modules. Module 1 aims to perform the different computations for the portfolio optimization. Module 2 aims to extract the calculations from Module 1, distribute them into the different Excel sheet to make them clear and intuitive. Plus, Module 2 extract the data from Yahoo Finance through Alphavantage, distribute them into the sheets to be then processed by Module 1. Finally, Module 4 aims to manage the different results within the different Excel sheets, generate charts...

### Module 1

![formula](Images/1.JPG)

Sub PortfOptProcess() aims to compute the potfolio optimization process. The first part of this Sub (see screenshot above) is initialize the different main parameters that are going to be used during the optimization process usch as the risk-free rate, the number of iterations, the number of stocks, initializing matrices that are going to be filled by optimization parameters such as portofolio returns, standard deviation, sharpe ratio etc.


## Model Limitations

Regarging our model several points can be pointed
