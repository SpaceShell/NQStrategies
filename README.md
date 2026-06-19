# NQStrategies
A collection of various NQ trading strategies for NinjaTrader that seamlessly automate contracts and can be imported to the NinjaTrader platform.

# Reference
## NQ Strategy
The NQ Strategy is a strategy that automates 2 contract buys/sells after 10 points in profit from when the previous contract enters.

### How It Works
1st Contract:
Entered by user. Initiates the strategy.
- All following contracts will be a buy if the first contract is a buy or a sell if the first contract is a sell

2nd Contract:
Enters after 10 points in profit from the 1st contract.
- Stop Loss: 7.5 pts
- Profit Target: 15 pts

3rd Contract
Enters after 10 points in profit from the 2nd contract.
- Stop Loss: 5 pts
- Profit Target: 15 pts

Strategy restarts after 3rd contract closes.

## NQ Scale
The NQ Scale is a variation of the NQ strategy that operates the same, but additionally includes breakevens after 10 points in profit from when the previous contract enters.

### How It Works
1st Contract:
Entered by user. Initiates the strategy.
- All following contracts will be a buy if the first contract is a buy or a sell if the first contract is a sell

2nd Contract:
Enters after 10 points in profit from the 1st contract.
- Stop Loss: 7.5 pts
- Profit Target: 15 pts

3rd Contract
Enters after 10 points in profit from the 2nd contract.
- At the same time that the contract enters, the stop loss of the 2nd Contract moves 0.5 pts in profit fromwhen it entered
- Stop Loss: 5 pts
- Profit Target: 15 pts
- After 10 points in profit, the stop loss of the 3rd Contract moves 0.5 pts in profit from when it entered

Strategy restarts after 3rd contract closes.

## MNQ Strategy

## NQ 2-Leg Strategy
