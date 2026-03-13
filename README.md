# Crypto Market Monitor

Comprehensive cryptocurrency market monitoring and economic data analysis skill for OpenClaw.

## Features

- **Price Monitoring**: Track 13 major cryptocurrencies (BTC, ETH, XRP, BNB, SOL, ADA, AVAX, DOGE, TRX, LINK, SUI, WLFI, XAUT) with real-time prices, volatility alerts (±5%), market sentiment analysis, and EMA technical indicators
- **Economic Calendar**: 7-day forecast of important economic data releases (CPI, NFP, FOMC, GDP, etc.)
- **Impact Analysis**: Automatic bullish/bearish determination based on actual vs expected values
- **Automated Reports**: Daily 08:00 economic forecasts + 30-min comprehensive monitoring

## Installation

### Option 1: From GitHub

```bash
# Clone the repository
git clone https://github.com/KJjjj0/crypto-market-skill.git

# Copy files to your OpenClaw workspace
cp -r crypto-market-skill/* ~/.openclaw/workspace/crypto/

# Set permissions
chmod +x ~/.openclaw/workspace/crypto/scripts/*.py
```

### Option 2: Download .skill file

Download the `.skill` file from the releases and install manually.

## Quick Start

### Price Monitoring
```bash
cd scripts
python3 crypto_monitor_telegram.py
```

### Economic Data Report
```bash
cd economic
python3 daily_economic_report_v2.py
```

### Update Economic Data
```bash
cd economic
python3 update_economic_data.py update "CPI 消费者价格指数" "2.1%"
```

## Economic Indicators

### High Importance
- Non-Farm Payrolls (NFP)
- CPI (Consumer Price Index)
- FOMC Interest Rate Decisions
- GDP (Gross Domestic Product)
- Unemployment Rate

### Medium Importance
- ADP Employment Data
- Retail Sales
- Manufacturing PMI
- Services PMI
- PPI (Producer Price Index)

## Bullish/Bearish Analysis

### Bullish Indicators (Higher is Better)
- NFP, GDP, Retail Sales, ADP, PMIs

**Rule**: Actual > Expected (+2%+) = Bullish 🟢

### Bearish Indicators (Lower is Better)
- CPI, PPI, Unemployment Rate, Interest Rates

**Rule**: Actual < Expected (-2%+) = Bullish 🟢 (pressure relief)

## Documentation

- [INSTALL.md](INSTALL.md) - Detailed installation guide
- [references/quick-reference.md](references/quick-reference.md) - Command cheat sheet
- [references/data-types.md](references/data-types.md) - Economic indicator details
- [references/usage-examples.md](references/usage-examples.md) - Real-world scenarios

## Requirements

- Python 3.6+
- requests
- pytz
- feedparser

## License

MIT

