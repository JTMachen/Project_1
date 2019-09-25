# Hacking The S&P 500: SPY ETF Time Series Analysis

###  by Vinay Kakuru, Roberto Cantu, Jonathan Machen, and Brent McMinn

## What (Objective):

This project aims to measure the hourly market behavior of the S&P 500 Total Return index by drawing inferences from the SPY ETF, which is constructed using full replication and has a tracking error of + 0.03%. 

## Why:

We realized there could potentially be a trend in behavior in the window from 2:30pm to 4:00pm. Therefore, we wanted to know if we could better predict when IN the 2:30pm-4:00pm window we were to see movement on a given day based on past historical data fed into our model, or of a different time window with similar behavior.

Taking each hour interval and comparing this time period to the other intervals of the same hour, over the course of months would give systematic traders insight into why certain intraday bins were more favorable than others for a given trading strategy.

With this information, investors could build time period specific strategies that only trade at certain times of the day depending on the market conditions. In theory, if there is a time period that offers better risk adjusted returns, investors would identify this set of conditions, and based on probabilities, would turn to trading algorithms to enter at more favorable time periods.

## How:

To begin, we grouped the data by each hour, from which we computed both the mean and standard deviation. From this, we built return distributions with about 12 daily periods worth of data for each hour. Therefore, we had 12 5-min. intervals per hour, 6.5 hours per day which gave us a total of 936 data points, or 144 data points for each hour. 

Then, through the plotting of the histograms and overlaying them on each other, we are able to show the skewed distributions of returns. We then examined these time periods in further detail by conducting t-tests to assess if their underlying statistical properties were different from each other at a significance level of 99%.