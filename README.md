# Gold Mini Demarker MT5

This code is a sample implementation of the Gold Mini Demarker MT5 trading strategy developed by Forex Robot Easy Team. The strategy combines the Risky Grid Strategy and Martingale Strategy to open positions based on technical indicators.

## Strategy Overview

The Gold Mini Demarker MT5 strategy is designed to open positions in the Gold market using a combination of the Risky Grid Strategy and Martingale Strategy. The strategy relies on three technical indicators: Moving Averages, Force Index, and DeMarker.

### Moving Averages

The Moving Averages indicator is used to smooth out price data. In this strategy, a simple moving average with a period of 14 is used to calculate the smoothed price.

### Force Index

The Force Index indicator is used to measure the raw power of a move. In this strategy, a Force Index with a period of 14 is used to calculate the force index value.

### DeMarker

The DeMarker indicator is used to compare the maximum and minimum prices with the close price. In this strategy, a DeMarker with a period of 14 is used to calculate the maximum price, minimum price, and close price.

## Trading Execution

The strategy executes trades based on the technical indicators. 

1. The strategy first checks if the maximum and minimum prices are surpassed by the close price using the ComparePrices() function.
2. If the maximum and minimum prices are surpassed, the strategy opens positions using the Risky Grid Strategy.
   - The number of orders to open is determined by the maxOrders variable.
   - The entry price for each order is calculated based on the current market bid price and the grid step (gridStep).
   - Each order is placed with a lot size of lotSize.
   - The comment for these orders is set as 'Risky Grid Strategy'.
3. After opening positions using the Risky Grid Strategy, the strategy opens additional positions using the Martingale Strategy.
   - The number of additional orders is determined by the martingaleMultiplier variable.
   - The entry price for each additional order is calculated based on the current market bid price and the grid step (gridStep).
   - The lot size for each additional order is multiplied by the order number (i).
   - The comment for these orders is set as 'Martingale Strategy'.

## Usage

To use this code, you will need to include the necessary libraries: Trade, MovingAverages, ForceIndex, and DeMarker. You will also need to initialize the necessary variables for lot size, maximum number of orders, grid step, and martingale multiplier. Finally, you will need to initialize the trading functions and technical indicators.

The code provides three helper functions:
- GetSmoothedPrice(): Returns the smoothed price calculated using the Moving Averages indicator.
- GetForceIndex(): Returns the force index value calculated using the Force Index indicator.
- ComparePrices(): Compares the maximum and minimum prices with the close price using the DeMarker indicator and returns a boolean value indicating if the close price surpasses the maximum or minimum prices.

The OnTick() function serves as the entry point of the program. It updates the technical indicators and executes trades based on the technical indicators.

## Product Description

Gold Mini Demarker MT5 is a trading strategy designed for the MetaTrader 5 platform. It combines the Risky Grid Strategy and Martingale Strategy to open positions in the Gold market.

The strategy is based on three technical indicators: Moving Averages, Force Index, and DeMarker. Moving Averages is used to smooth out price data, Force Index is used to measure the raw power of a move, and DeMarker is used to compare the maximum and minimum prices with the close price.

The strategy opens positions when the close price surpasses the maximum or minimum prices. It first opens positions using the Risky Grid Strategy, and then opens additional positions using the Martingale Strategy. The lot size for the positions can be customized, and the strategy can open up to a maximum number of orders. 

Please note that Forex Robot Easy is not the official developer of this product. We only provide a sample implementation of the strategy based on the provided code. For detailed reviews and trading results of this product, please visit [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/gold-mini-demarker-mt5-review-risky-grid-martingale-strategy/). To find the official developer of this product, please use the MQL5 platform.
