# Strategy Research: 5-Minute Scalping Indicator (VWAP TFC Model)

Based on the video by Sean Solano: "This 5 Minute Scalping Indicator Made Me $11,790 This Week"

## Overview
The strategy is a trend-following scalping model that uses **VWAP** as the primary indicator to identify momentum and entry points. It relies on the **TFC (Trend Failure Continuation)** model.

## Setup
- **Timeframe**:
    - Entry: 5-Minute chart.
    - Bias: 1-Hour or 4-Hour chart.
- **Indicators**:
    - **VWAP (Volume Weighted Average Price)**: The core indicator. Settings: Only the VWAP line (blue) is used; upper/lower bands are removed.
    - **9 EMA (Exponential Moving Average)**: Used as a trailing stop or exit signal for longer holds.

## Strategy Rules

### 1. Market Bias (HTF)
- Determine the overall trend on the 1-hour or 4-hour chart.
- Only trade in the direction of the HTF trend.

### 2. Entry Model: TFC (Trend Failure Continuation)
- **Step 1**: Price crosses VWAP.
- **Step 2**: Price retests VWAP (fails to cross back significantly or shows rejection).
- **Step 3**: Entry on the break of the candle's high/low that confirmed the continuation.
    - *Example for Shorts*: Price breaks below VWAP -> Retests VWAP -> Breaks the low of the retest candle.

### 3. Filters
- **Avoid Flat VWAP**: Do not trade when the VWAP line is horizontal (indicates consolidation/low volume).
- **Seek Sharp Moves**: Look for steep VWAP slopes indicating strong momentum.

### 4. Risk Management
- **Stop Loss**:
    - Placed on the other side of VWAP.
    - Or above/below the previous candle's high/low.
- **Take Profit**:
    - HTF liquidity areas (previous swing highs/lows).
    - 50% Fibonacci retracement levels.
    - Exit when price closes on the opposite side of the 9 EMA or VWAP.

## Summary of TFC Logic
1. **Trend**: Move in direction of HTF.
2. **Fail**: Price attempts to move against VWAP or stalls at it.
3. **Continue**: Price breaks through and continues, confirming the momentum.
