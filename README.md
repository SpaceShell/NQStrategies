# NQStrategies
A collection of various NQ trading strategies for NinjaTrader that seamlessly automate contracts and can be imported to the NinjaTrader platform.

## Table of Contents | All Strategies
- [NQ Strategy](#nq-strategy)
- [NQ Scale](#nq-scale)
- [MNQ Strategy](#mnq-strategy)
- [NQ 2-Leg Strategy](#nq-2-leg-strategy)

## NQ Strategy
The NQ Strategy is a strategy that automates 2 contract buys/sells after 10 pts (points) in profit from the previous entry.

### How It Works
**1st Entry (1 Contract):**
Entered by user. Initiates the strategy.
- All following entries will be a buy if the first entry is a buy or a sell if the first entry is a sell

**2nd Entry (1 Contract):**
Enters after 10 pts in profit from the 1st entry.
- Stop Loss: 7.5 pts
- Profit Target: 15 pts

**3rd Entry (1 Contract):**
Enters after 10 pts in profit from the 2nd entry.
- Stop Loss: 5 pts
- Profit Target: 15 pts

Strategy restarts after 3rd entry closes.

## NQ Scale
The NQ Scale is a variation of the [NQ Strategy](#nq-strategy) strategy. It operates the same, but additionally includes breakevens after 10 pts in profit from the previous entry.

### How It Works
**1st Entry (1 Contract):**
Entered by user. Initiates the strategy.
- All following entries will be a buy if the first entry is a buy or a sell if the first entry is a sell

**2nd Entry (1 Contract):**
Enters after 10 pts in profit from the 1st entry.
- Stop Loss: 7.5 pts
- Profit Target: 15 pts

**3rd Entry (1 Contract):**
Enters after 10 pts in profit from the 2nd entry.
- Breakeven: At the same time of the 3rd Entry, the stop loss of the 2nd Entry moves 0.5 pts in profit from when it entered
- Stop Loss: 5 pts
- Profit Target: 15 pts
- Breakeven: After 10 pts in profit, the stop loss of the 3rd Entry moves 0.5 pts in profit from when it entered

Strategy restarts after 3rd entry closes.

## MNQ Strategy
The MNQ Strategy (or the Micro NQ Strategy) is a micro version of the [NQ Strategy](#nq-strategy) strategy that enters 5 contracts instead of 1 per entry and has both larger stop losses and profit targets. Additionally, it includes breakevens after 20 pts in profit from the previous entry, similarly to [NQ Scale](#nq-scale).

### How It Works
**1st Entry (5 Contracts):**
Entered by user. Initiates the strategy.
- All following entries will be a buy if the first entry is a buy or a sell if the first entry is a sell

**2nd Entry (5 Contracts):**
Enters after 10 pts in profit from the 1st entry.
- Stop Loss: 14 pts
- Profit Target: 30 pts

**3rd Entry (5 Contracts):**
Enters after 10 pts in profit from the 2nd entry.
- Breakeven: After 20 pts in profit, the stop loss of the 2nd Entry moves 0.5 pts in profit from when it entered
- Stop Loss: 10 pts
- Profit Target: 30 pts
- Breakeven: After 20 pts in profit, the stop loss of the 3rd Entry moves 0.5 pts in profit from when it entered

Strategy restarts after 3rd entry closes.

## NQ 2-Leg Strategy
The NQ 2-Leg Strategy is a variation of the MNQ Strategy with 2 entries instead of 3 entries, a 5 pt change for the 2nd Entry, and a breakeven of 1 pt in profit for the 2nd Entry.

### How It Works
**1st Entry (5 Contracts):**
Entered by user. Initiates the strategy.
- All following entries will be a buy if the first entry is a buy or a sell if the first entry is a sell

**2nd Entry (5 Contracts):**
Enters after 5 pts in profit from the 1st entry.
- Stop Loss: 14 pts
- Profit Target: 30 pts
- Breakeven: After 10 pts in profit, the stop loss of the 2nd Entry moves 1 pts in profit from when it entered

Strategy restarts after 2nd entry closes.
