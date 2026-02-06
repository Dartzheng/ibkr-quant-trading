# IBKR Quantitative Trading Platform

A comprehensive quantitative trading analysis and model training platform for Interactive Brokers (IBKR).

## 🎯 Project Overview

This platform provides tools and models for:
- Algorithmic trading strategy development
- Backtesting and performance analysis
- Machine learning model training for market prediction
- Real-time trading execution via IBKR API
- Risk management and portfolio optimization

## 📁 Project Structure

```
ibkr-quant-trading/
├── data/              # Market data storage
├── models/            # Trained ML models
├── strategies/        # Trading strategies
├── backtests/         # Backtesting results
├── notebooks/         # Jupyter notebooks for analysis
├── src/               # Source code
│   ├── data_fetcher/  # Data collection modules
│   ├── features/      # Feature engineering
│   ├── models/        # ML model implementations
│   ├── backtester/    # Backtesting engine
│   └── trader/        # Live trading execution
├── tests/             # Unit tests
├── configs/           # Configuration files
└── docs/              # Documentation
```

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- IBKR TWS or IB Gateway
- IBKR API credentials

### Installation

```bash
# Clone the repository
git clone https://github.com/Dartzheng/ibkr-quant-trading.git
cd ibkr-quant-trading

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Configuration

1. Copy `configs/config.example.yaml` to `configs/config.yaml`
2. Add your IBKR API credentials
3. Configure trading parameters

## 📊 Features

### Data Collection
- Real-time market data streaming
- Historical data download
- Multiple asset classes support (stocks, options, futures)

### Strategy Development
- Technical indicator library
- Signal generation framework
- Custom strategy templates

### Model Training
- Feature engineering pipeline
- Multiple ML algorithms (Random Forest, XGBoost, LSTM)
- Hyperparameter optimization
- Model evaluation metrics

### Backtesting
- Event-driven backtesting engine
- Transaction cost modeling
- Performance analytics
- Risk metrics calculation

### Live Trading
- Automated order execution
- Position management
- Risk controls and limits
- Real-time monitoring

## 📈 Usage Examples

### Fetch Historical Data

```python
from src.data_fetcher import IBKRDataFetcher

fetcher = IBKRDataFetcher()
data = fetcher.get_historical_data(
    symbol='AAPL',
    duration='1 Y',
    bar_size='1 day'
)
```

### Run Backtest

```python
from src.backtester import Backtester
from strategies.mean_reversion import MeanReversionStrategy

strategy = MeanReversionStrategy()
backtester = Backtester(strategy)
results = backtester.run(start_date='2023-01-01', end_date='2024-01-01')
```

### Train ML Model

```python
from src.models import LSTMPredictor

model = LSTMPredictor()
model.train(data, epochs=100)
model.save('models/lstm_v1.h5')
```

## 🛡️ Risk Management

- Maximum position size limits
- Daily loss limits
- Volatility-based position sizing
- Stop-loss and take-profit automation

## 📝 Development Roadmap

- [ ] Set up IBKR API connection
- [ ] Implement data fetching pipeline
- [ ] Build feature engineering module
- [ ] Develop backtesting framework
- [ ] Train baseline ML models
- [ ] Create strategy templates
- [ ] Implement live trading engine
- [ ] Add performance monitoring dashboard
- [ ] Write comprehensive tests
- [ ] Deploy to production

## 🤝 Contributing

This is a personal project. Feel free to fork and adapt for your own use.

## ⚠️ Disclaimer

This software is for educational and research purposes only. Trading involves substantial risk. Past performance does not guarantee future results. Always conduct thorough testing before deploying any strategy with real capital.

## 📄 License

MIT License - see LICENSE file for details

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.
