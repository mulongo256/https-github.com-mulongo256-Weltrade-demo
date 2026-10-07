# https-github.com-mulongo256-Weltrade-demoBROKER = "Weltrade"
SERVER = "Weltrade-Real"

DNS_SERVERS = [
    "mt5.dc1.weltrade.com",
    "mt5.dc2.weltrade.com",
]

ALLOWED_SYMBOLS = [
    "MAX GainX 2000",
    "MAX PainX 2000",
    "PainX 1200",
    "PainX 600",
    "PainX 800",
    "PainX 999",
    "GainX 600",
    "GainX 800",
    "GainX 999",
    "GainX 1200",
    "GainX 400",
    "MAX GainX 1000",
    "MAX PainX 1000",
    "PainX 400",
]

TIMEFRAMES = [
    "M1", "M2", "M3", "M4", "M5",
    "M15", "M20", "M30", "M45", "H1"
]

RSI_PERIOD = 10
BUY_ZONE = (0.0, 10.0)
SELL_ZONE = (90.0, 100.0)

TP1_RSI = 50.0
BUY_INVALIDATION_RSI = 0.0
SELL_INVALIDATION_RSI = 100.0

ALLIGATOR_TEETH_PERIOD = 7
ALLIGATOR_TEETH_SHIFT = 0
ALLIGATOR_LIPS_PERIOD = 1000
ALLIGATOR_LIPS_SHIFT = 800
ALLIGATOR_METHOD = "LWMA"
ALLIGATOR_PRICE = "weighted_close"

ICHIMOKU_TENKAN = 1
ICHIMOKU_KIJUN = 1
ICHIMOKU_SENKOU_B = 1

BEARS_POWER_PERIOD = 80000

SIGNAL_ONLY = True
REQUIRE_ALL_10 = True
pandas>=2.2
numpy>=1.26
requests>=2.32
from config import (
    BROKER,
    SERVER,
    ALLOWED_SYMBOLS,
    TIMEFRAMES,
    SIGNAL_ONLY
)

print("================================")
print("     WELTRADE REVERSAL AI")
print("================================")
print("Broker:", BROKER)
print("Server:", SERVER)
print("Signal only:", SIGNAL_ONLY)

print("\nAllowed symbols:")
for symbol in ALLOWED_SYMBOLS:
    print("-", symbol)

print("\nRequired timeframes:")
print(", ".join(TIMEFRAMES))

print("\nBUY zone: RSI 0-10")
print("SELL zone: RSI 90-100")
print("TP1: RSI 50")
print("BUY invalidation: RSI 0")
print("SELL invalidation: RSI 100")

print("\n10/10 timeframe confirmation required.")
print("No automatic trading.")

print("\nLIVE MARKET DATA: NOT CONNECTED YET")
print("Codespace configuration is ready.")
{
  "name": "Weltrade Reversal AI",
  "image": "mcr.microsoft.com/devcontainers/python:1-3.11-bookworm",
  "postCreateCommand": "pip install --upgrade pip && pip install -r requirements.txt",
  "customizations": {
    "vscode": {
      "extensions": [
        "ms-python.python",
        "ms-python.vscode-pylance"
      ]
    }
  }
}
